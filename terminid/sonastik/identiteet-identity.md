# identiteet \(identity\)

## Definitsioon

{% hint style="info" %}
garanteeritult unikaalne ja konstantne väärtus mis ei muutu [objekti ](objekt-object.md)eluea jooksul
{% endhint %}

## Täpsemalt

Igal [objektil](objekt-object.md) on identiteet, tüüp ja väärtus. Objekti identiteet ei muutu kunagi peale loomist, sellest võib mõelda kui objekti aadressist mälus. Kaks objekti mille eluiga ei kattu võivad omada sama identiteeti \(s.t. et identiteete võidakse taaskasutada\).'

`is` operaator võrdleb kahe objekti identiteete; `id()` funktsioon tagastab täisarvu \(_integer_\) mis esitab \(_representing_\) objekti identideedi.

CPythoni teostuse \(_implementation_\) detail: identiteet on objekti aadress mälus.

Objekti tüüp \(_type_\) mõjutab identiteeti. [Muutumatute](muutumatu-immutable.md) \(_immutable_\) tüüpide korral võib tehe millega arvutatakse uus väärtus tagastada viite juba olemasolevale objektile mille tüüp ja väärtus on samad, samas kui [muudetavate](muudetav-mutable.md) \(_mutable_\) objektide korral pole see lubatud. See tähendab, et peale `a = 1; b = 1` nimed `a` ja `b`  võivad või mitte \(_may or may not_\)  viidata samale objektile väärtusega `1`  \(sõltuvalt lahendusest\) aga peale `c = []; d = []` on garanteeritud et `c` ja `d` viitavad kahele erinevale, unikaalsele ja äsja loodud tühjale loendile \(_list_\).

```python
>>> a = []
>>> b = []
>>> a is b
False           # objektide identiteet on erinev
>>> a == b 
True            # objektide väärtus on sama
```

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; The Python Language Reference &gt; 3. Data model &gt; [3.1. Objects, values and types  ](https://docs.python.org/3/reference/datamodel.html#objects-values-and-types)
* Documentation &gt; The Python Standard Library &gt; Built-in Functions &gt;  [id\(_object_\)](https://docs.python.org/3/library/functions.html#id)

