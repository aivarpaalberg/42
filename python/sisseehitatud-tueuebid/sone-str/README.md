---
description: 'Teksti jada tüüp (Text Sequence Type), Pythoni sisseehitatud andmetüüp.'
---

# sõne \(str\)

## Tähendus

{% hint style="info" %}
Pythonis on sõne \(_str_\) teksti jada tüüp \(_text sequence type_\) üks sisemistest \(_built-in_\) [andmetüüpidest](../../../terminid/sonastik/andmetueuep-datatype.md) \(_datatypes_\). 
{% endhint %}

## Täpsemalt

Tekstilisi andmeid käsitsetakse \(_handled_\) Pythonis `str` objektidega ehk sõnedega \(_string_\). Sõned \(_strings_\) on Unicode koodipunktide **muutumatud** \(immutable\) **jadad** \(sequences\).

Sõne \(_string_\) [literaale](../../../terminid/sonastik/literaal-literal.md) \(_literals_\) kirjutatakse erinevatel viisidel:

* ülakomaga jutumärgiga \(_single quotes_\): `'võimaldab sõnes kasutada "kahe ülakomaga" jutumärki'`
* kahe ülakomaga jutumärgiga \(_double quotes_\): `"võimaldab sõnes kasutada 'ülakomaga' jutumärki"`
* jutumärgid kolmekordselt \(_triple quoted_\): `'''kolm ülakomaga jutumärki'''`, `"""kolm kahe ülakomaga jutumärki"""`

Ülakomaga jutumärgiga \(_single quotes_\) sõnedes saab kasutada kasutada ülakoma ja kahe ülakomaga jutumärgiga \(_double quotes_\) saab kasutada kahte ülekoma kui kasutada märgi ees paomärki \(_escape character_\) `\` :

```python
>>> s = 'sõnes võib kasutada \'ühte ülakoma\' kasutades paomärki'
>>> s
"sõnes võib kasutada 'ühte ülakoma' kasutades paomärki"
>>> s = "sõnes võib kasutada \"kahte ülakoma\" kasutades paomärki"
>>> s
'sõnes võib kasutada "kahte ülakoma" kasutades paomärki'
```

Kolmekordsetes jutumärkides sõned võivad ulatuda üle mitme rea ning säilivad kõik sõnes esinevad mitteväljastatavad märgid \(tühikud, reavahetused jms\).

```python
>>> spam = """
... see
...     on
...        trepp
... """
>>> print(spam)

see
    on
       trepp

>>>
```

Sõne [literaalid](../../../terminid/sonastik/literaal-literal.md) \(_literals_\), mis  on ühe [avaldise](../../../terminid/sonastik/avaldis-expression.md) \(_expression_\) osad ning mille vahel on ainult tühikud \(_whitespace_\) teisendatakse \(_converted_\) ilmutamata \(_implicitly_\) üheks sõne literaaliks:

```python
>>> 'abra' 'kad' 'abra'
'abrakadabra'
>>> 'abra' 'kad' 'abra' == 'abrakadabra'
True
```

Sõnesid \(_strings_\) saab luua ka teistest objektidest kasutades str konstuktorit.

Ei ole olemas [muudetavat](../../../terminid/sonastik/muudetav-mutable.md) \(_mutable_\) sõne tüüpi kuid [str.join\(\)](untitled/str.join.md) ja io.StringIO\(\) saab efektiivselt kasutada erinevate sõnede konstrueerimiseks üheks sõneks.

