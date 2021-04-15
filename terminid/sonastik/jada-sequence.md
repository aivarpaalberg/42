# jada \(sequence\)

## Tähendus

{% hint style="info" %}
[Itereeritav](itereeritav-iterable.md) mis toetab tõhusat \(_efficient_\) ligipääsu elementidele kasutades täisarvu \(_integer_\) indekseid läbi `__getitem__()`spetsiaalmeetodi ja mis defineerib `__len__()` meetodi mis tagastab jada pikkuse.
{% endhint %}

## Täpsemalt

Mõned Pythoni sisemised \(_built-in_\) **jada tüübid** on [loend](loend-list.md) \(_list_\), [sõne](../../python/sisseehitatud-tueuebid/sone-str/) \(_str_\), ennik \(_tuple_\) ja baidid \(_bytes_\). Pange tähele, et [sõnastik](sonastik-dictionary.md) \(_dict_\) toetab ka `__getitem__()`  ja `__len__()` kuid seda loetakse vastenduseks \(_mapping_\) ja mitte jadaks \(_sequence_\) kuna pöördumiseks kasutatakse suvalisi \(_arbitrary_\) [muutumatuid](muutumatu-immutable.md) \(_immutable_\) võtmeid ja mitte täisarve \(_integers_\).

`collections.abc.Sequence` abstraktne baasklass \(_abstract base class_\) defineerib märksa rikkalikuma liidese \(_interface_\) kui ainult `__getitem__()` ja `__len__()` lisades `count()` , `index()` , `__contains__()` ja `__reversed__()`. [Tüübid](andmetueuep-datatype.md) \(_types_\) mis teostavad \(_implement_\) seda laiendatud liidest saab ilmutatult \(_explicitly_\) registreerida kasutades `register()` .

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [sequence](https://docs.python.org/3/glossary.html#term-sequence)  

