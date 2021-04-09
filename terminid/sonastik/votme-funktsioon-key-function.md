# võtme funktsioon \(key function\)

## Tähendus

{% hint style="info" %}
võtme funktsioon \(_key function_\) või võrdlusfunktsioon \(_collation function_\) on väljakutsutav  \(_callable_\) mis tagastab väärtuse \(_value_\) mida kasutatakse sortimiseks \(_sorting_\) ja järjestamiseks \(_ordering_\).
{% endhint %}

## Täpsemalt

Mitmed Pythoni instrumendid \(_tools_\) aktsepeteerivad võtme funktsiooni määramaks kuidas elemendid on järjestatud või grupeeritud. Nende hulgas on `min()`, `max()`, `sorted()` , `list.sort()`, `heapq.merge()`, `heapq.nsmallest()`, `heapq.nlargest()` ja `itertools.groupby()` . 

Võtme funktsiooni \(_key function_\) saab luua mitmel erineval moel. Näiteks võib `str.lower()` [meetodit](meetod-method.md) kasutada võtme funktsioonina tõstutundetul sortimisel \(_case insensitive sort_\). Alternatiivselt võib võtme funktsiooni luua kasutates `lambda` [avaldist](avaldis-expression.md) \(_expression_\), näiteks `lambda r: (r[0], r[2])` . Lisaks pakub `operator` moodul kolme võtme funktsiooni konstruktorit \(_constructors_\): `attrgetter()` , `itemgetter()` ja `methodcaller()` .

## Viited 

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [key function](https://docs.python.org/3/glossary.html#term-key-function)
* Documentation &gt; Python HOWTOs &gt; [Sorting HOW TO](https://docs.python.org/3/howto/sorting.html#sortinghowto)



