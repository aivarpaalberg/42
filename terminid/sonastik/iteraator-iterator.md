# iteraator \(iterator\)

## Tähendus

{% hint style="info" %}
[Objekt ](objekt-object.md)mis esitab \(_representing_\) andmete voo \(_stream_\).
{% endhint %}

## Täpsemalt

Iteraatori `__next__()`  meetodi korduvad väljakutsumised \(või edastades selle sisseehitatud funktsioonile `next()` \) tagastavad üksteisele järgnevaid  voo elemente. Kui rohkem andmeid \(_data_\) ei ole saadaval tõstetakse selle asemel `StopIteration` erand. Sel hetkel on iteraator objekt \(_iterator object_\) ammendunud \(_exchausted_\) ja mistahes edaspidised `__next__()` meetodi väljakutsed tõstavad jälle `StopIteration` erandi.

Iteraatoritel peab olema `__iter__()` meetod mis tagastab iteraatori objekti enda nii, et iga iteraator on ka itereeritav ja seda võib kasutada enamikes kohtades kus itereeritavaid vastu võetakse \(_accepted_\). Üks märkimisväärne erand on kood mis proovib mitmekordset iteraatori läbimist. [Konteiner](konteiner-container.md) objekt \(_container object_\) nagu näiteks loend \(_list_\) loob uue iteraatori iga kord kui see edastatakse `iter()` funktsioonile või kasutamaks `for` silmuses \(_loop_\). Üritades seda iteraatoriga tagastatakse vaid sama ammendunud \(_exhausted_\) iteraator objekti mida kasutati eelmise iteratsiooni läbimisel mistõttu näib see olevat nagu tühi [konteiner](konteiner-container.md).

 Repeated calls to the iterator’s [`__next__()`](https://docs.python.org/3/library/stdtypes.html#iterator.__next__) method \(or passing it to the built-in function [`next()`](https://docs.python.org/3/library/functions.html#next)\) return successive items in the stream. When no more data are available a [`StopIteration`](https://docs.python.org/3/library/exceptions.html#StopIteration) exception is raised instead. At this point, the iterator object is exhausted and any further calls to its `__next__()` method just raise [`StopIteration`](https://docs.python.org/3/library/exceptions.html#StopIteration) again. Iterators are required to have an [`__iter__()`](https://docs.python.org/3/reference/datamodel.html#object.__iter__) method that returns the iterator object itself so every iterator is also iterable and may be used in most places where other iterables are accepted. One notable exception is code which attempts multiple iteration passes. A container object \(such as a[`list`](https://docs.python.org/3/library/stdtypes.html#list)\) produces a fresh new iterator each time you pass it to the [`iter()`](https://docs.python.org/3/library/functions.html#iter) function or use it in a [`for`](https://docs.python.org/3/reference/compound_stmts.html#for)loop. Attempting this with an iterator will just return the same exhausted iterator object used in the previous iteration pass, making it appear like an empty container.

More information can be found in [Iterator Types](https://docs.python.org/3/library/stdtypes.html#typeiter).

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [iterator](https://docs.python.org/3/glossary.html#term-iterator)

