# itereeritav \(iterable\)

## Tähendus

{% hint style="info" %}
[objekt](objekt-object.md), mis on võimeline tagastama oma liikmeid ühekaupa. 
{% endhint %}

## Täpsemalt

Itereeritavateks on näiteks kõik[ jada](jada-sequence.md) tüübid \(_sequence type_\) nagu [loend](loend-list.md) \(_list_\), [sõne](../../python/sisseehitatud-tueuebid/sone-str/) \(_str_\) ja ennik \(_tuple_\) ning mõned mitte-jada tüübid nagu [sõnastikud](sonastik-dictionary.md) \(_dict_\), failobjektid \(_file object_\) ning objektid mistahes enda defineeritud klassist `__iter()__()` meetodiga või `__getitem__()` meetodiga mis teostab \(_implements_\) [jada](jada-sequence.md) \(_sequence_\) semantika \(_semantics_\) 

Itereeritavaid saab kasutada `for` [silmuses](silmus-loop.md) \(_loop_\) ja paljudes teistes kohtades kus on vajalik [jada](jada-sequence.md) \(_sequence_\) nagu näiteks `zip()` , `map()` jne.

Kui itereeritav [objekt](objekt-object.md) edastatakse sisemisele \(_built-in_\) [funktsioonile](funktsioon-function.md) `iter()` [argumendina](argument.md) tagastatakse objekti [iteraator](iteraator-iterator.md) \(_iterator_\). Seda iteraatori väärtuste hulka saab läbida üks kord peale mida on ta ammendunud \(_exhausted_\).

Itereeritavate kasutamisel ei ole tavaliselt vaja välja kutsuda funktsiooni `iter()` või käsitleda \(_deal_\) [iteraator](iteraator-iterator.md) objekte otse. `for` [lause](lause-statement.md) \(_statement_\) teeb seda sinu jaoks automaatselt luues ajutise \(_temporary_\) nimetu \(_unnamed_\) muutuja \(_variable_\) iteraatori hoidmiseks silmuse korduste ajaks \(_for duration of the loop_\).

Vaata ka [iteraator](iteraator-iterator.md) \(_iterator_\), [jada](jada-sequence.md) \(_sequence_\) ja [generaator](generaator-generator.md) \(_generator_\).

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [iterable](https://docs.python.org/3/glossary.html#term-iterable)  

