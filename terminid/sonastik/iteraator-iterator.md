# iteraator \(iterator\)

## Tähendus

{% hint style="info" %}
[objekt ](objekt-object.md)mis esitab \(_representing_\) andmete voo \(_stream_\).
{% endhint %}

## Täpsemalt

Iteraatori `__next__()`  [meetodi](meetod-method.md) korduvad väljakutsumised \(või edastades selle sisemisele funktsioonile `next()` \) tagastavad üksteisele järgnevaid  voo elemente. Kui rohkem [andmeid](andmed-data.md) \(_data_\) ei ole saadaval tõstetakse selle asemel `StopIteration` erand. Sel hetkel on iteraator objekt \(_iterator object_\) ammendunud \(_exchausted_\) ja mistahes edaspidised `__next__()` [meetodi](meetod-method.md) väljakutsed tõstavad jälle `StopIteration` erandi.

Iteraatoritel peab olema `__iter__()` [meetod](meetod-method.md) mis tagastab iteraatori objekti enda nii, et iga iteraator on ka [itereeritav](itereeritav-iterable.md) \(_iterable_\) ja seda võib kasutada enamikes kohtades kus itereeritavaid vastu võetakse \(_accepted_\). Üks märkimisväärne erand on kood mis proovib mitmekordset iteraatori läbimist. [Konteiner](konteiner-container.md) objekt \(_container object_\) nagu näiteks [loend](loend-list.md) \(_list_\) loob uue iteraatori iga kord kui see edastatakse `iter()` funktsioonile või kasutamaks `for` silmuses \(_loop_\). Üritades seda iteraatoriga tagastatakse vaid sama ammendunud \(_exhausted_\) iteraator objekti mida kasutati eelmise iteratsiooni läbimisel mistõttu näib see olevat nagu tühi [konteiner](konteiner-container.md).

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [iterator](https://docs.python.org/3/glossary.html#term-iterator)

