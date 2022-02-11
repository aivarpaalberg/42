# Abiinfo leidmine

[Programmeerimiskeele](../terminid/sonastik/programmeerimiskeel-programming-language.md#taehendus) (_programming language_) õppimine on sarnane [loomuliku](../terminid/sonastik/loomulik-keel-natural-language.md#taehendus) võõrkeele õppimisele.&#x20;

[Loomuliku](../terminid/sonastik/loomulik-keel-natural-language.md#taehendus) võõrkeele omandamiseks tuleb ühekorraga meelde jätta tohutu hulk informatsiooni - sõnad, nende jagunemine nimi-, omadus- ja tegusõnadeks koos pööramise-käänamisega, sõnade järjestusega lauses ning ajavormidega. Ilma nende teadmisteta on raske ennast arusaadavalt väljendada. Aga rääkida tahaks enne kui see kõik selgeks on saadud.

Sarnases olukorras on ka [programmeerimiskeele](../terminid/sonastik/programmeerimiskeel-programming-language.md#taehendus) õppija, vahe on ainult selles, et tegu on [tehiskeelega](../terminid/sonastik/tehiskeel-artificial-language.md#taehendus) (_artificial language_).&#x20;

Võrreldes loomuliku keelega on tehiskeele reeglid selgesõnaliselt kehtestatud eesmärgiga välistada mitmetähenduslikkus. Seetõttu on reeglite täpne täitmine programmeerimiskeele kasutamisel äärmiselt oluline. Inimesed võtavad omavahelises suhtluses arvesse konteksti ja sõnadel võib olla mitu tähendust aga programmeerimiskeele puhul saab arvuti olenemata kontekstist käsklusest alati ühte moodi aru. Iseasi on muidugi see, kas arvuti käsku täites teeb seda, mida käskluse kirjutaja soovis.

Loomuliku võõrkeele õppimisel on abiks sõnaraamatud ja (grammatika)õpikud. Mida võiks kasutada Pythoni õppija? Kuidas leiab Pythoniga alustaja vajalikku abiinfot?&#x20;

Kui eestikeelsest ja küllaltki napist materjalist ei leia vastuseid esilekerkinud küsimusele siis mida teha? Esimene millega peab arvestama on vajadus ümber lülituda inglise keelele. Eestikeelset materjali on tõesti vähe ja Pythoni ametlik abiinfo on inglise keeles. Samas ei pea kohe tormama [python.org](https://www.python.org) või [stackoverflow.com](https://stackoverflow.com) lehele vaid alustada võib Pythoni sisemisest abiinfost mis on saadaval [interaktiivses interpretaatoris](../terminid/sonastik/interaktiivne-interactive.md#taehendus) (hoiatus: abiinfo kvaliteet on kõikuv). Sisemise abiinfoni jõuab kasutades sisemist help() funktsiooni:

```bash
>>> help()

Welcome to Python 3.10's help utility!

If this is your first time using Python, you should definitely check out
the tutorial on the internet at https://docs.python.org/3.10/tutorial/.

Enter the name of any module, keyword, or topic to get help on writing
Python programs and using Python modules.  To quit this help utility and
return to the interpreter, just type "quit".

To get a list of available modules, keywords, symbols, or topics, type
"modules", "keywords", "symbols", or "topics".  Each module also comes
with a one-line summary of what it does; to list the modules whose name
or summary contain a given string such as "spam", type "modules spam".

help>
```

Abiinfost väljumiseks vajuta `Q` klahvi (see viib tagasi [interaktiivsesse interpretaatorisse](../terminid/sonastik/interaktiivne-interactive.md#taehendus))

Abiinfo otsimiseks ei pea 'sisenema' help keskonda vaid saab anda `help()` funktsioonile argumendi. Sellisel moel abiinfot otsides tuleb silmas pidada, et nimesid (s.h. sisemised [objektid](../terminid/sonastik/objekt-object.md#taehendus), funktsioonid, meetodid) tuleb otsida nii nagu neid kirjutatakse ja võtmesõnu jms aga [sõne literaalina](sisseehitatud-tueuebid/sone-str/#taepsemalt).

```bash
>>> help(max)
Help on built-in function max in module builtins:

max(...)
    max(iterable, *[, default=obj, key=func]) -> value
    max(arg1, arg2, *args, *[, key=func]) -> value

    With a single iterable argument, return its biggest item. The
    default keyword-only argument specifies an object to return if
    the provided iterable is empty.
    With two or more arguments, return the largest argument.

```

Sõnena:

```
>>> help('if')
The "if" statement
******************

The "if" statement is used for conditional execution:

   if_stmt ::= "if" assignment_expression ":" suite
               ("elif" assignment_expression ":" suite)*
               ["else" ":" suite]

It selects exactly one of the suites by evaluating the expressions one
by one until one is found to be true (see section Boolean operations
for the definition of true and false); then that suite is executed
(and no other part of the "if" statement is executed or evaluated).
If all expressions are false, the suite of the "else" clause, if
present, is executed.

Related help topics: TRUTHVALUE

```

Kui on vaja teada, millised on mingi [andmetüübi](../terminid/sonastik/andmetueuep-datatype.md#taehendus) või selle [eksemplari](../terminid/sonastik/eksemplar-instance.md#taehendus) (instance) meetodid siis on nende leidmine interaktiivses interpretaatoris äärmiselt lihtne (alljärgnev on eksemplari kohta, andmetüübi puhul tuleb kasutada selle nime koos punktiga nt str., list. jne):

```
spam = 'abc'
>>> s.            # vajuta 2 x TAB klahvi
s.capitalize()   s.format(        s.isidentifier() s.ljust(         s.rfind(         s.startswith(
s.casefold()     s.format_map(    s.islower()      s.lower()        s.rindex(        s.strip(
s.center(        s.index(         s.isnumeric()    s.lstrip(        s.rjust(         s.swapcase()
s.count(         s.isalnum()      s.isprintable()  s.maketrans(     s.rpartition(    s.title()
s.encode(        s.isalpha()      s.isspace()      s.partition(     s.rsplit(        s.translate(
s.endswith(      s.isascii()      s.istitle()      s.removeprefix(  s.rstrip(        s.upper()
s.expandtabs(    s.isdecimal()    s.isupper()      s.removesuffix(  s.split(         s.zfill(
s.find(          s.isdigit()      s.join(          s.replace(       s.splitlines(
```

Kui on vaja aru saada, mida mingi meetod teeb siis saab jälle help() poole pöörduda:

```
>>> help(s.capitalize)
Help on built-in function capitalize:

capitalize() method of builtins.str instance
    Return a capitalized version of the string.

    More specifically, make the first character have upper case and the rest lower
    case.
```

Sama käib ka imporditud moodulite kohta:

```
>>> import string
>>> string.
string.ascii_letters   string.capwords(       string.hexdigits       string.punctuation
string.ascii_lowercase string.digits          string.octdigits       string.Template(
string.ascii_uppercase string.Formatter()     string.printable       string.whitespace
```

NB! kasutades `from string import *` imporditakse funtsioonid nimeruumi ilma mooduli nimeta ning eelpooltoodud moel pole meetodeid/abiinfot võimalik saada.

string puhul tagastavad meetodid väärtuse ja tegelikku abiinfot ei saagi (vt eelpool toodud hoiatust abiinfo kvaliteedi kohta):

```python
>>> help(string.punctuation)
No Python documentation found for '!"#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~'.
Use help() to get the interactive help utility.
Use help(str) for help on the str class.
```

