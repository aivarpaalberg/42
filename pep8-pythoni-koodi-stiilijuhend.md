# PEP8 - Pythoni koodi stiilijuhend

## Sissejuhatus

See dokument annab [kodeerimise](terminid/sonastik/kodeerimine-coding.md) \(_coding_\) tavad \(_conventions_\) Pythoni koodile peamise \(_main_\) Pythoni distributsiooni standard teegis \(_standard library_\). Palun vaadake kaasnevat informatiivset PEP-i, mis kirjeldab C-koodi stiilijuhiseid Pythoni C-teostuses \(_C implementation of Python_\).

See dokument ja PEP 257 \(Docstring Conventions\) on kohandatud Guido algsest Pythoni stiilijuhendi esseest koos mõne täiendusega Barry stiilijuhendist.

See stiilijuhend areneb ajas, kuna tuvastatakse \(_identified_\) täiendavaid tavasid  ja olemasolevad tavad    aeguvad muutuste tõttu keeles endas. 

Paljudel projektidel on oma kodeerimisstiili juhised. Mis tahes konfliktide korral on sellised projektispetsiifilised juhendid selle projekti jaoks ülimuslikud.

## Väikest mõistust painab rumal järjepidevus

Guido üks võtmekaemusi on see, et koodi loetakse palju sagedamini kui seda kirjutatakse. Siin toodud juhiste eesmärk on parandada koodi loetavust ja ühtlustada Pythoni koodi kogu selle laias spektris. Nagu PEP 20 ütleb: "Loetavus loeb".

Stiilijuhend on järjepidevusest. Järjepidevus stiilijuhendi järgimisel on tähtis. Projektisisene järjepidevus on tähtsam. Järjepidevus moodulis või funktsioonis on kõige tähtsam.

Aga tea, milla olla ebajärjekindel - mõnikord ei ole stiilijuhendi soovitused lihtsalt rakendatavad.  Kui kahtled, kasuta oma parimat äranägemist. Vaata teisi näiteid ja otsusta, mis kõige paremini välja näeb. Ja ära karda küsida!

Eriti: ära katkesta tagasiühilduvust \(_backward compatibility_\) ainult selle PEP järgmiseks.

Mõned muud head põhjused konkreetse stiilijuhise eiramiseks:

1. Kui stiilijuhise rakendamine muudaks koodi vähem loetavaks isegi kellelegi, kes on harjunud lugema koodi mis järgib käesolevat PEP-i.
2. Et olla kooskõlas ümbritseva koodiga, mis samuti seda rikub \(võib-ollo ajaloolistel põhjustel\) - kuigi see on ka hea võimalus koristada kellegi teise järelt \(tõelises XP stiilis\)
3. Kuna kõnealune kood eelnes stiilijuhendi kasutuselevõtule ja selle koodi muutmiseks pole muud põhjust.
4. Kui kood peab jääma ühilduvaks Pythoni vanemate versioonidega, mis ei toeta stiilijuhendis soovitatud erisust \(_feature_\).

## Koodi paigutus

### Taane

Kasuta 4 tühikut taande taseme kohta.



### Tabeldus või tühikud?

Tühikud \(_spaces_\) on eelistatud taandemeetod.

Tabeldust \(_tab_\) tuleks kasutada ainult selleks, et need oleksid kooskõlas koodiga, mis on juba tabeldusega taandatud.

Python 3 keelab taandamisel tabelduste ja tühikute segamini kasutamise.

Python 2 kood, mis on taandatud läbisegi tabelduste ja tühikutega tuleks teisendada ainult tühikuid kasutavaks.

Käivitades Python 2 käsurea interpretaatori `-t` valikuga, annab see hoiatusi koodi kohta, mis kasutab keelatult tabeldusi ja tühikuid läbisegi. Kasutades `-tt` valikut muutuvad need hoiatused vigadeks. Need valikud on väga soovitatavad!

### Rea maksimaalpikkus

Piira kõigi ridade pikkust maksimaalselt 79 märgiga.

### Kas reavahetus peaks olema enne või peale binaaroperaatorit?

### Tühjad read

### Lähtefaili kodeering

### Importimine

### Mooduli  taseme tala nimed

## Sõne jutumärgid

## Tühik avaldistes ja lausetes

### Tüütused

### Muud soovitused

## Millal kasutada järelkoma

## Kommentaarid

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



