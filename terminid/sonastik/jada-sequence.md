# jada (sequence)

## Tähendus

Infotehnoloogias ja Pythonis on jadal (_sequence_) erinev tähendus.

{% hint style="info" %}
**Infotehnoloogia:** [jadastatud](jadastama-to-sequence.md) (_sequenced_) üksuste (_items_) sari (_series_)

**Python:** [itereeritav](itereeritav-iterable.md) mis toetab tõhusat (_efficient_) ligipääsu [elementidele](element-element.md) kasutades täisarvu (_integer_) indekseid läbi `__getitem__()`spetsiaalmeetodi ja mis defineerib `__len__()` meetodi mis tagastab jada pikkuse.
{% endhint %}

Pythoni jadadel (_sequences_) on jadastatud (_sequenced_) elementide indeksid ja mitte jada elemendid ise.

## Täpsemalt

Mõned Pythoni sisemised (_built-in_) **jada tüübid** on [loend](loend-list.md) (_list_), [sõne](../../python/sisseehitatud-tueuebid/sone-str/) (_str_), ennik (_tuple_) ja baidid (_bytes_). Pane tähele, et [sõnastik](sonastik-dictionary.md) (_dict_) toetab ka `__getitem__()`  ja `__len__()` kuid seda loetakse vastenduseks (_mapping_) ja mitte jadaks (_sequence_) kuna pöördumiseks kasutatakse suvalisi (_arbitrary_) [muutumatuid](muutumatu-immutable.md) (_immutable_) võtmeid ja mitte täisarve (_integers_).

`collections.abc.Sequence` abstraktne baasklass (_abstract base class_) defineerib märksa rikkalikuma liidese (_interface_) kui ainult `__getitem__()` ja `__len__()` lisades `count()` , `index()` ,` __contains__()` ja `__reversed__()`. [Tüübid](andmetueuep-datatype.md) (_types_) mis teostavad (_implement_) seda laiendatud liidest saab ilmutatult (_explicitly_) registreerida kasutades `register()` .

## Viited

Pythoni ametlik dokumentatsioon (inglise keeles):

* Documentation > Glossary > [sequence](https://docs.python.org/3/glossary.html#term-sequence)

[EVS-ISO 2382-6:1999](https://www.evs.ee/et/evs-iso-2382-6-1999), Infotehnoloogia. Sõnastik. Osa 6: Andmevalmendus ja andmekäitlus:

* [jada (_sequence_)](http://www.eki.ee/dict/its/index.cgi?Q=D0A7AEA3-6C03-1014-88DC-FC5F0DBED45A\&F=GUID\&C01=1\&C02=0\&C10=1)\
  \
