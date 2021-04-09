# võtme funktsioon \(key function\)

## Tähendus

{% hint style="info" %}
võtme funktsioon \(_key function_\) või võrdlusfunktsioon \(_collation function_\) on väljakutsutav  \(_callable_\) mis tagastab väärtuse \(_value_\) mida kasutatakse sortimiseks \(_sorting_\) ja järjestamiseks \(_ordering_\).
{% endhint %}

## Täpsemalt

Mitmed Pythoni instrumendid \(_tools_\) aktsepeteerivad võtme funktsiooni kontrollimaks kuidas elemendid on järjestatud või grupeeritud. Nende hulgas on `min()`, `max()`, `sorted()` , `list.sort()`, `heapq.merge()`, `heapq.nsmallest()`, `heapq.nlargest()` ja `itertools.groupby()` . 

Võtme funktsiooni \(_key function_\) saab luua mitmel erineval moel. Näiteks võib `str.lower()` kasutada võtme funktsioonina 

A key function or collation function is a callable that returns a value used for sorting or ordering. For example, [`locale.strxfrm()`](https://docs.python.org/3/library/locale.html#locale.strxfrm) is used to produce a sort key that is aware of locale specific sort conventions.

A number of tools in Python accept key functions to control how elements are ordered or grouped. They include [`min()`](https://docs.python.org/3/library/functions.html#min), [`max()`](https://docs.python.org/3/library/functions.html#max), [`sorted()`](https://docs.python.org/3/library/functions.html#sorted), [`list.sort()`](https://docs.python.org/3/library/stdtypes.html#list.sort), [`heapq.merge()`](https://docs.python.org/3/library/heapq.html#heapq.merge), [`heapq.nsmallest()`](https://docs.python.org/3/library/heapq.html#heapq.nsmallest), [`heapq.nlargest()`](https://docs.python.org/3/library/heapq.html#heapq.nlargest), and [`itertools.groupby()`](https://docs.python.org/3/library/itertools.html#itertools.groupby).

There are several ways to create a key function. For example. the [`str.lower()`](https://docs.python.org/3/library/stdtypes.html#str.lower) method can serve as a key function for case insensitive sorts. Alternatively, a key function can be built from a [`lambda`](https://docs.python.org/3/reference/expressions.html#lambda)expression such as `lambda r: (r[0], r[2])`. Also, the [`operator`](https://docs.python.org/3/library/operator.html#module-operator) module provides three key function constructors: [`attrgetter()`](https://docs.python.org/3/library/operator.html#operator.attrgetter), [`itemgetter()`](https://docs.python.org/3/library/operator.html#operator.itemgetter), and [`methodcaller()`](https://docs.python.org/3/library/operator.html#operator.methodcaller). See the [Sorting HOW TO](https://docs.python.org/3/howto/sorting.html#sortinghowto) for examples of how to create and use key functions.

