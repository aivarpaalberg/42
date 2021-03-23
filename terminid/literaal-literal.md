---
description: >-
  Pythoni literaalid on mõnede sissehitatud (built-in) andmetüüpide (data types)
  konstantsete väärtuste tähistused.
---

# literaal \(literal\)

## Üksikasjalikumalt

Teisiti öeldes on literaal väärtus mis on kirjutatud nii nagu seda interpreteeritakse programmi poolt s.t literaali väärtust ei ole vaja arvutada; tegu on objektiga mille väärtus ei sõltu teiste muutujate \(objektide\) väärtustest ja nende muutumistest ning mis ei sisalda tehet.

Python toetab [sõne](../python/sisseehitatud-tueuebid/sone-str/) \(_str_\) ja baidi \(_bytes_\) literaale ning mitmeid numbri \(_numeric_\) literaale:

```python
literal ::= stringliterals | bytesliterals | integer | floatnumber | imagnumber
```

Literaali hindamine \(_evaluation_\) annab \(_yields_\) antud tüüpi objekti \(sõne, baidid, täisarv, ujukomaarv, kompleksarv\) selle väärtusega. Väärtus võib olla ligikaudne ujukomaarvude ja imaginaararvude \(kompleksarvude\) puhul.

Kõik Pythoni literaalid on muutumatud \(_immutable_\) mistõttu objekti identiteet on vähem tähtis kui selle väärtus. Sama väärtusega literaalide mitmekordsed hindamised \(evaluations\) võivad saada \(\_obtain-\) sama objekti või teise objekti sama väärtusega.

Literaalide näited:

```python
'tere' # sõne
42     # täisarv
4.2    # ujukomaarv
```

Väärtused mida tuleb arvutada \([avaldised](avaldis-expression.md)\) ei ole literaalid. Oluline on teada, et Pythoni numbrilised literaalid ei sisalda märki. Selle tõttu on märkidega numbrid [avaldised](avaldis-expression.md) \(_expressions_\) ning mitte literaalid:

```python
1 + 3    # avaldis mis koosneb kahest literaalist ja tehtemärgist
-42      # avaldis mis koosneb unaarsest tehtemärgist ja literaalist
```

Unaarne tehtemärk on madalama prioriteediga kui astendamine ning seetõttu on annab astendamine esmapailgul ebaloogilise tulemuse:

```python
>>> -2**2        # kõigepealt astendamine ja siis unaarne tehtemärk   
-4           
>>> (-2)**2      # kõigepealt unaarse tehtemärgiga avaldise väärtuse arvutamine ja seejärel astendamine
4
```

Identifikaatorid \(nimed\) ei ole literaalid. Püüdes kasutada literaali nimena tõstab Python `SyntaxError` erandi:

```python
>>> 'tere' = 1
  File "<stdin>", line 1
SyntaxError: can't assign to literal
>>> 1 = 'tere'
  File "<stdin>", line 1
SyntaxError: can't assign to literal
```

### Viited

* [The Python Language Reference &gt;&gt;&gt; 2. Lexical Analysis &gt;&gt;&gt; 2.4. Literals](https://docs.python.org/3/reference/lexical_analysis.html#literals)
* [The Python Language Reference &gt;&gt;&gt; 6. Expressions &gt;&gt;&gt; 6.2.2. Literals](https://docs.python.org/3/reference/expressions.html#literals)
* [The story of None, True and False \(and an explanation of literals, keywords and builtins thrown in\) by Guido van Rossum](http://python-history.blogspot.com/2013/11/story-of-none-true-false.html)

