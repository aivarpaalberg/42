# PEP8 - Pythoni koodi stiilijuhend

## Sissejuhatus

See dokument annab [kodeerimise](terminid/sonastik/kodeerimine-coding.md) \(_coding_\) tavad \(_conventions_\)  peamise \(_main_\) Pythoni distributsiooni standard teegi \(_standard library_\) [koodile](terminid/sonastik/kood-code.md). Palun vaata kaasnevat informatiivset PEP-i, mis kirjeldab C-koodi stiilijuhiseid Pythoni C-teostuses \(_C implementation of Python_\).

See dokument ja PEP 257 \(Docstring Conventions\) on kohandatud Guido algsest Pythoni stiilijuhendi esseest koos mõne täiendusega Barry stiilijuhendist.

See stiilijuhend areneb ajas, kuna tuvastatakse \(_identified_\) täiendavaid tavasid  ja olemasolevad tavad    aeguvad muutuste tõttu keeles endas. 

Paljudel projektidel on oma kodeerimisstiili juhised. Mis tahes konfliktide korral on sellised projektispetsiifilised juhendid selle projekti jaoks ülimuslikud.

## Väikest mõistust painab rumal järjepidevus

Guido üks võtmekaemusi on see, et [koodi](terminid/sonastik/kood-code.md) loetakse palju sagedamini kui seda kirjutatakse. Siin toodud juhiste eesmärk on parandada koodi loetavust ja ühtlustada Pythoni koodi kogu selle laias spektris. Nagu PEP 20 ütleb: "Loetavus loeb".

Stiilijuhend on järjepidevusest \(_consistency_\). Järjepidevus stiilijuhendi järgimisel on tähtis. Projektisisene järjepidevus on tähtsam. Järjepidevus [moodulis](terminid/sonastik/moodul-module.md) või [funktsioonis](terminid/sonastik/funktsioon-function.md) on kõige tähtsam.

Aga tea, millal olla ebajärjekindel - mõnikord ei ole stiilijuhendi soovitused lihtsalt rakendatavad.  Kui kahtled, kasuta oma parimat äranägemist. Vaata teisi näiteid ja otsusta, mis kõige paremini välja näeb. Ja ära karda küsida!

Eriti: ära katkesta tagasiühilduvust \(_backward compatibility_\) ainult selle PEP-i järgimiseks.

Mõned muud head põhjused konkreetse stiilijuhise eiramiseks:

1. Kui stiilijuhise rakendamine muudaks [koodi](terminid/sonastik/kood-code.md) vähem loetavaks isegi kellelegi, kes on harjunud lugema koodi mis järgib käesolevat PEP-i.
2. Et olla kooskõlas ümbritseva koodiga, mis samuti seda rikub \(võib-olla ajaloolistel põhjustel\) - kuigi see on ka hea võimalus koristada kellegi teise järelt \(tõelises XP stiilis\)
3. Kuna kõnealune kood eelnes stiilijuhendi kasutuselevõtule ja selle koodi muutmiseks pole muud põhjust.
4. Kui kood peab jääma ühilduvaks Pythoni vanemate versioonidega, mis ei toeta stiilijuhendis soovitatud erisust \(_feature_\).

## Koodi paigutus

### Taane

Kasuta 4 [tühikut](terminid/sonastik/tuehik-space-character.md) taande taseme kohta.



### Tabeldus või tühikud?

[Tühikud](terminid/sonastik/tuehik-space-character.md) \(_spaces_\) on eelistatud taandemeetod.

Tabeldusi \(_tab_\) tuleks kasutada ainult selleks, et need oleksid kooskõlas [koodiga](terminid/sonastik/kood-code.md), mis on juba tabeldusega taandatud.

Python 3 keelab taandamisel tabelduste ja [tühikute](terminid/sonastik/tuehik-space-character.md) segamini kasutamise.

Python 2 kood, mis on taandatud läbisegi tabelduste ja tühikutega tuleks teisendada ainult tühikuid kasutavaks.

Käivitades Python 2 käsurea interpretaatori `-t` valikuga, annab see hoiatusi koodi kohta, mis kasutab keelatult tabeldusi ja tühikuid läbisegi. Kasutades `-tt` valikut muutuvad need hoiatused vigadeks. Need valikud on väga soovitatavad!

### Rea maksimaalpikkus

Piira kõigi ridade pikkust maksimaalselt 79 [märgiga](terminid/sonastik/maerk-character.md).

### Kas reavahetus peaks olema enne või peale binaaroperaatorit?

### Tühjad read

### Lähtefaili kodeering

### Importimine

Importimine peaks tavaliselt toimuma eraldi ridadel:

```python
# Õige
import os
import sys
```

```python
# Vale
import os, sys
```

Siiski on sedasi öelda OK:

```python
# Õige
from subprocess import Popen, PIPE
```

Importimised pannakse alati [faili](terminid/sonastik/fail-file.md) algusesse, kohe peale mooduli kommentaare ja [dokumentatsiooni sõnet](terminid/sonastik/dokumentatsiooni-sone-docstring.md) ning enne mooduli [globaale](terminid/sonastik/globaalne-global.md) \(_global_\) ja [konstante](terminid/sonastik/konstant-constant.md) \(_constants_\).

Importimised tuleks grupeerida järgnevas järjestuses:

1. Standardteegi \(_standard library_\) importimised
2. Seotud \(_related_\) kolmanda osapoole \(_third party_\) importimised
3. Kohaliku rakenduse \(_application_\) / teegi \(_library_\) spetsiifilised importimised

Peaksid panema tühja rea iga importimise grupi vahele.

* soovitavad on absoluutsed importimised \(_absolute imports_\), kuna need on tavaliselt loetavamad ja kalduvad \(_tend to_\) paremini käituma \(_be better behaved_\) \(või vähemalt annavad paremaid veateateid\) kui importimise süsteem on valesti konfigureeritud \(nagu siis kui paketisisene kataloog \(_directory_\) lõpetab `sys.path` peal\):

```python
import mypkg.sibling
from mypkg import sibling
from mypkg.sibling import example
```

Siiski on ilmutatud \(_explicit_\) suhtleline \(_relative_\) importimine aksepteeritav alternatiiv absoluutsele importimisele, eriti kui tegu on komplekse paketi paigutusega \(_layout_\), kus absoluutse importimise kasutamine oleks liigselt paljusõnaline \(_verbose_\):

```python
from . import sibling
from .sibling import example
```

Standardteegi \(_standrd library_\)  [kood](terminid/sonastik/kood-code.md) \(_code_\) peaks vältima keerukaid paketipaigutusi ja kasutama alati absoluutset importimist.

Ilmutamata \(_implicit_\) suhtelist \(_relative_\) importimist ei tohiks _kunagi_ kasutada ja see on Python 3-st eemaldatud.

Klassi importimisel klassi sisaldavast moodulist on tavaliselt OK kirjutada nii:

```python
from myclass import MyClass
from foo.bar.yourclass import YourClass
```

Kui selline kirjaviis põhjustab kohalike \(_local_\) nimede konflikte \(_clash_\) siis kirjutage need ilmutatult \(_explicitly_\):

```python
import myclass
import foo.bar.yourclass
```

ning kasutage `myclass.MyClass` ja  `foo.bar.yourclass.YourClass`.

Tärniga importimist \(`from <module> import *`\) tuleks vältida kuna see muudab ebaselgeks millised [nimed](terminid/sonastik/nimi-name.md) \(_names_\) [nimeruumis](terminid/sonastik/nimeruum-namespace.md) \(_namespace_\) esinevad, eksitades nii lugejaid kui ka paljusid automatiseeritud tööriistu \(_tools_\). Tärniga importimiseks on üks õigustatav \(_defencible_\) kasutusjuhtum \(_use case_\), milleks on sisemise liidese \(_internal interface_\) taasavaldamine \(_republish_\) avaliku API osana \(näiteks puhtas Pythonis teostatud liidese ülekirjutamine definitsiooniga valikulisest kiirendi moodulist \(_optional accelerator module_\) kui ei ole täpselt ette teada millised definitsioonid üle kirjutatakse\)

Nimede \(_names_\) sellisel viisil taasavaldamisel \(_republish_\) kehtivad ikkagi allpool toodud juhised avalike \(_public_\) ja sisemiste \(_internal_\) liideste kohta. 

### Mooduli  taseme tala nimed

## Sõne jutumärgid

## Tühik avaldistes ja lausetes

### Tüütused

Väldi tühikuid järgmistes olukordades:

* Vahetult sulgude \(_parentheses_\), nurksulgude \(_brackets_\), nurgeliste sulgude \(_braces_\) sees:

```python
# Õige

spam(ham[1], {eggs: 2})
```

```python
# Vale

spam( ham[ 1 ], { eggs: 2 } )
```

* Järelkoma ja lõpetava sulu vahel:

```python
# Õige

foo = (0,)
```

```python
# Vale

foo = (0, )
```

* vahetult enne koma \(_comma_\), semikoolonit \(_semicolon_\) või koolonit \(_colon_\):

```python
# Õige

if x == 4: print x, y; x, y = y, x
```

```python
# Vale

if x == 4 : print x , y ; x , y = y , x
```

### Muud soovitused

## Millal kasutada järelkoma

Järelkomad \(_trailing commas_\) on tavaliselt valikulised \(_optional_\) välja arvatud juhul, kui luua ühe elemendiga ennik \(_tuple_\), mille puhul on järelkoma kohustuslik \(ja Python 2-s on neil semantika `print` [lause](terminid/sonastik/lause-statement.md) \(_statement_\) jaoks\). Selguse huvides on soovitav ümbritseda viimane \(tehniliselt liigsete\) sulgudega \(_parantheses_\).

```python
# Õige

FILES = ('setup.cfg',)
```

```python
# Vale

FILES = 'setup.cfg',
```

Kui järelkomad on üleliigsed \(_redundant_\), on neist sageli kasu versioonihaldussüsteemi kasutamisel, kui eeldatakse, et väärtuste \(_values_\), argumentide \(_arguments_\) või imporditud \(_imported_\) üksuste \(_items_\) loetelu pikeneb aja jooksul. Mustriks on  panna iga väärtus \(vms\) eraldi reale, lisades alati järelkoma ja pannes sulud \(_parantheses_\) / nurksulud \(_brackets_\) / nurgelised sulud \(_braces_\) järgmisele reale. Kuid pole mõtet omada järelkoma samal real kui sulgev eraldaja \(_closing delimiter_\) \(välja arvatud ülaltoodud üksiku elemendiga ennikute puhul\):

```python
# Õige

FILES = [
    'setup.cfg',
    'tox.ini',
    ]
initialize(FILES,
           error=True,
           )
```

```python
# Vale

FILES = ['setup.cfg', 'tox.ini',]
initialize(FILES, error=True,)
```

## Kommentaarid

Kommentaarid, mis on vastuolus koodiga, on halvemad kui kood ilma kommentaarideta. Koodi muutumisel sea alati prioriteediks kommentaaride hoidmine ajakohasena!

Kommentaarid peaksid olema täislaused. Esimene sõna peaks algama suurtähega, välja arvatud juhul, kui see on [identifikaator](terminid/sonastik/identifikaator-identifier.md) \(_identifier_\), mis algab väiketähega \(ära kunagi muuda identifikaatorite tähti!\). 

Plokk kommentaarid \(_block comments_\) koosnevad üldjuhul ühest või enamast lõigust \(_paragraph_\) mis on koostatud täislausetest, mis kõik lõppevad punktiga \(_period_\).

Mitme lausega kommentaarides peaksid lause järel kasutama kahte tühikut, välja arvatud viimase lause järel.

Veenduge, et kommentaarid oleksid selged ja kergesti mõistetavad teistele selles keeles kõnelejatele, milles kirjutate.

### Plokk kommentaarid

### Reasisesed kommentaarid

### Dokumentatsiooni sõned

## Nimetamise tavad

### Valdav printsiip

### Kirjeldav: nimetamise stiilid

### Normatiivne: nimetamise tavad

#### Nimed mida vältida

#### ASCII ühilduvus

#### Pakettide ja moodulite nimed

#### Klassi nimed

#### Tüübimuutujate nimed

#### Erandite nimed

#### Globaalsete muutujate nimed

#### Funktsioonide ja muutujate nimed

#### Funktsioonide ja meetodite argumendid

#### Meetodite nimed ja eksemplari muutujad

#### Konstandid

#### Kavandamine pärilikkuse jaoks

### Avalikud ja sisemised liidesed

## Programmeerimise soovitused

### Funktsioonide ääremärkused

### Muutujate ääremärkused

## Viited

## Autoriõigus







## Viited:

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Python &gt; Python Developer's Guide &gt; PEP Index &gt; [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)´´



