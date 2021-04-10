# dokumentatsiooni sõne \(docstring\)

## Tähendus

{% hint style="info" %}
[sõne](../../python/sisseehitatud-tueuebid/sone-str/) \(_string_\) [literaal](literaal-literal.md) \(_literal_\) mis ilmub kui esimene [avaldis](avaldis-expression.md) \(_expression_\) [klassis](klass-class.md), [funktsioonis](funktsioon-function.md) või moodulis.
{% endhint %}

## Täpsemalt

Kuigi dokumentatsiooni sõnet \(_docstring_\) ignoreeritakse kui komplekti \(_suite_\) [täidetakse](taeitmine-execution.md) \(_executed_\) tunneb kompilaator \(_compiler_\) selle ära ja paneb selle  ümbritseva \(_enclosing_\) [klassi](klass-class.md), [funktsiooni](funktsioon-function.md) või mooduli `__doc__` [atribuuti](atribuut-attribute.md). Kuna tegu on käideldava \(_available_\) atribuudiga siis on see kanooniline \(_canonical_\) koht objekti dokumentatsiooni jaoks.

Kooskõla \(_consistency_\) tagamiseks tuleks dokumentatsiooni sõnede \(_docstrings_\) ümber alati kasutada kolmekordeid kahe ülakomaga [jutumärke](jutumaergid.md) \(_triple double quotes_\). 

Kasuta `r"""töötlemata sõnet (raw string) kolmekordsete kahe ülakomaga jutumärkide vahel"""`  kui dokumentatsiooni sõnes esineb kurakaldkriips \(`\`\). 

Kasuta `u"""Unicode sõnet kolmekordete kahe ülakomaga jutumärkide vahel"""`kui tegu on Unicode vormingus dokumentatsiooni sõnega.

Dokumentatsiooni sõned \(_docstrings_\) on kahes vormis: üherealine \(_one-liners_\) ja mitmerealine \(_multi-line_\). 

Kõigil moodulitel peaks tavaliselt olema dokumentatsioon sõne \(_docstring_\) ja kõik funktsioonid ning klassid mida eksporditakse mooduliga peaksid samuti omama dokumentatsioon sõne. Avalikel meetoditel \(_public methods_\) s.h. `__init__`  __konstruktoril peaks samuti  olema dokumentatsiooni sõne. Pakett \(_package_\) võib olla dokumenteeritud mooduli dokumentatsiooni sõnes \(`__init__.py` fail paketi kataloogis\) 

Sõne [literaalid](literaal-literal.md) \(_string literals_\) mis esinevad mujal Pythoni koodis võivad samuti toimimida kui dokumentatsioon. Pythoni baitkoodi kompilaator \(_bytecode compiler_\) ei tunne neid ära ja seetõttu pole nad ligipääsetavad kui käitusaegsed objekti atribuudid \(_runtime object attributes_\) s.t. neid ei omistata \(_assign_\) `__doc__` atribuudina, kuid tarkvaraliste vahenditega \(_software tools_\) on võimalik eraldada täiendavalt kahte tüüpi dokumentatsiooni sõnesid \(_docstrings_\):

1. Sõne [literaale](literaal-literal.md) \(_string literals_\) mis esinevad kohe peal lihtsat omistamist \(_simple assignment_\) mooduli, klassi või `__init__` meetodi kõrgeimal tasemel \(_top level_\) nimetatakse _atribuudi dokumentatsiooni sõneks_ \(_attribute docstring_\). 
2. Sõne literaale \(_string literals_\) mis esinevad kohe peale teist dokumentatsiooni sõne \(_docstring_\) kutsutakse täiendavateks dokumentatsiooni sõnedeks \(_additional docstrings_\)

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [docstring](https://docs.python.org/3/glossary.html#term-docstring)
* [PEP 257 -- Docstring Conventions](https://www.python.org/dev/peps/pep-0257/)

