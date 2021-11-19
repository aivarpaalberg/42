# doksõne (docstring)

## Tähendus

{% hint style="info" %}
[sõne](../../python/sisseehitatud-tueuebid/sone-str/) (_string_) [literaal](literaal-literal.md) (_literal_) mis ilmub kui esimene [avaldis](avaldis-expression.md) (_expression_) [klassis](klass-class.md) (_class_), [funktsioonis](funktsioon-function.md) (_function_) või [moodulis](moodul-module.md) (_module_).
{% endhint %}

## Täpsemalt

Kuigi doksõnet (_docstring_) ignoreeritakse kui komplekti (_suite_) [täidetakse](taeitmine-execution.md) (_executed_) tunneb kompilaator (_compiler_) selle ära ja paneb selle  ümbritseva (_enclosing_) [klassi](klass-class.md), [funktsiooni](funktsioon-function.md) või [mooduli](moodul-module.md) `__doc__` [atribuuti](atribuut-attribute.md). Kuna tegu on käideldava (_available_) atribuudiga siis on see kanooniline (_canonical_) koht objekti dokumentatsiooni jaoks.

Kooskõla (_consistency_) tagamiseks tuleks doksõnede (_docstrings_) ümber alati kasutada kolmekordeid kahe ülakomaga [jutumärke](jutumaergid.md) (_triple double quotes_).&#x20;

Kasuta `r"""töötlemata sõnet (raw string) kolmekordsete kahe ülakomaga jutumärkide vahel"""`  kui dokusnes esineb kurakaldkriips (`\`).&#x20;

Kasuta `u"""Unicode sõnet kolmekordete kahe ülakomaga jutumärkide vahel"""`kui tegu on Unicode vormingus doksõnega.

Doksõned (_docstrings_) on kahes vormis: [üherealine](dokumentatsiooni-sone-docstring.md#ueherealised-dokusoned) (_one-liners_) ja [mitmerealine](dokumentatsiooni-sone-docstring.md#mitmerealised-dokusoned) (_multi-line_).&#x20;

Kõigil [moodulitel](moodul-module.md) peaks tavaliselt olema doksõne (_docstring_) ja kõik [funktsioonid](funktsioon-function.md) ning [klassid](klass-class.md) mida eksporditakse mooduliga peaksid samuti omama doksõnet. Avalikel meetoditel (_public methods_) s.h. `__init__`_  _konstruktoril peaks samuti  olema doksõne. [Pakett](pakett-package.md) (_package_) võib olla dokumenteeritud [mooduli](moodul-module.md) doksõnes (`__init__.py` fail paketi kataloogis)&#x20;

Sõne [literaalid](literaal-literal.md) (_string literals_) mis esinevad mujal Pythoni koodis võivad samuti toimimida kui dokumentatsioon. Pythoni baitkoodi kompilaator (_bytecode compiler_) ei tunne neid ära ja seetõttu pole nad ligipääsetavad kui käitusaegsed objekti atribuudid (_runtime object attributes_) s.t. neid ei omistata (_assign_) `__doc__` [atribuudina](atribuut-attribute.md), kuid tarkvaraliste vahenditega (_software tools_) on võimalik eraldada täiendavalt kahte tüüpi dokusõnesid (_docstrings_):

1. Sõne [literaale](literaal-literal.md) (_string literals_) mis esinevad kohe peal lihtsat omistamist (_simple assignment_) [mooduli](moodul-module.md), [klassi](klass-class.md) või `__init__` [meetodi](meetod-method.md) kõrgeimal tasemel (_top level_) nimetatakse _atribuudi doksõneks_ (_attribute docstring_).&#x20;
2. Sõne [literaale](literaal-literal.md) (_string literals_) mis esinevad kohe peale teist doksõne (_docstring_) kutsutakse _täiendavateks doksõnedeks_ (_additional docstrings_)

## Üherealised doksõned

Üherealised (_one liners_) doksõned (_docstrings_), nii nagu nimi ütleb, peavad mahtuma ühele reale:

```python
def function(
```

Pane tähele:

* Kasutatakse kolmekordseid kahe ülakomaga [jutumärke](jutumaergid.md) kuigi sõne mahub ühele reale. Nii kirjutades teeb see ridade [lisamise](lisamine-insert.md) (_insert_) lihtsaks.
* Sulgevad jutumärgid on samal real kui alustavad jutumärgid. See näeb üherealiste (_one-liners_) puhul parem välja.
* Enne ega pärast doksõnet ei ole tühja rida.
* Doksõne (_docstring_) on fraas mis lõpeb punktiga. See määrab [funktsiooni](funktsioon-function.md) või [meetodi](meetod-method.md) toime (_effect_) kui käsu (_command_) s.t. `Tee...` , `Tagasta..` ja mitte kui kirjelduse (_description_). Seetõttu ära kirjuta `Tagastab..`&#x20;
* Üherealine doksõne (_one-line docstring_) ei peaks olema "signatuur" mis kordab [funktsiooni](funktsioon-function.md)/[meetodi](meetod-method.md) [parameetreid](parameeter-parameter.md) (mida võib saada sisevaatlusega (_introspection_)). Ära tee nii:

```python
def function(a, b):
    """function(a, b) -> list"""
```

## Mitmerealised doksõned

Mitmerealised doksõned (_multi-line docstring_) sisaldavad sarnaselt [üherealistele doksõnedele](dokumentatsiooni-sone-docstring.md#ueherealised-doksoned) lühikokkuvõtte rida (_summary line_) millele järgneb tühi rida, millele järgneb täpsem kirjeldus. Lühikokkuvõtte rida (_summary line_) võivad kasutada automaatsete indekseerimise vahendid; on tähtis, et see mahuks ühele reale ja tühi rida eraldaks seda ülejäänud doksõnest (_docstring_). Lühikokkuvõtte rida (_summary line_) võib olla alustavate [jutumärkidega](jutumaergid.md) samal või järgmisel real. Kogu doksõne (_docstring_) on taandatud sama palju kui alustavad jutumärgid esimeses reas (vaata näidet allpool):

Lisa (_insert_) tühi rida peale kõiki doksõnesid (nii üherealisi kui mitmerealisi) mis dokumenteerivad [klassi](klass-class.md) - üldistatult öeldes on klassi [meetodid](meetod-method.md) eraldatud üksteisest ainsa tühja reaga ja doksõne ise peab olema eraldatud esimesest meetodist tühja reaga.



The docstring of a script (a stand-alone program) should be usable as its "usage" message, printed when the script is invoked with incorrect or missing arguments (or perhaps with a "-h" option, for "help"). Such a docstring should document the script's function and command line syntax, environment variables, and files. Usage messages can be fairly elaborate (several screens full) and should be sufficient for a new user to use the command properly, as well as a complete quick reference to all options and arguments for the sophisticated user.

The docstring for a module should generally list the classes, exceptions and functions (and any other objects) that are exported by the module, with a one-line summary of each. (These summaries generally give less detail than the summary line in the object's docstring.) The docstring for a package (i.e., the docstring of the package's \_\_init\_\_.py module) should also list the modules and subpackages exported by the package.

The docstring for a function or method should summarize its behavior and document its arguments, return value(s), side effects, exceptions raised, and restrictions on when it can be called (all if applicable). Optional arguments should be indicated. It should be documented whether keyword arguments are part of the interface.

The docstring for a class should summarize its behavior and list the public methods and instance variables. If the class is intended to be subclassed, and has an additional interface for subclasses, this interface should be listed separately (in the docstring). The class constructor should be documented in the docstring for its \_\_init\_\_ method. Individual methods should be documented by their own docstring.

If a class subclasses another class and its behavior is mostly inherited from that class, its docstring should mention this and summarize the differences. Use the verb "override" to indicate that a subclass method replaces a superclass method and does not call the superclass method; use the verb "extend" to indicate that a subclass method calls the superclass method (in addition to its own behavior).

_Do not_ use the Emacs convention of mentioning the arguments of functions or methods in upper case in running text. Python is case sensitive and the argument names can be used for keyword arguments, so the docstring should document the correct argument names. It is best to list each argument on a separate line. For example:\
\


## Viited

Pythoni ametlik dokumentatsioon (inglise keeles):

* Documentation > Glossary > [docstring](https://docs.python.org/3/glossary.html#term-docstring)
* [PEP 257 -- Docstring Conventions](https://www.python.org/dev/peps/pep-0257/)
