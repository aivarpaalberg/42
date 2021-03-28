---
description: 'objektid mida tagastavad dict.keys(), dict.values() ja dict.items()'
---

# sõnastiku vaade \(dictionary view\)

## Üksikasjalikumalt

Sõnastiku vaate objektid pakuvad \(_provide_\) sõnastiku kirjete \(_dictionary's entries_\) dünaamilist vaadet \(_dynamic view_\) mis tähendab, et kui sõnastik muutub siis vaade peegeldab neid muutusi. Sundimaks \(to force\) sõnastiku vaadet muutuma loendiks \(_list_\) kasuta `list(dictview)` 

```python
>>> d = dict(enumerate('abc', start=1))
>>> d
{1: 'a', 2: 'b', 3: 'c'}
>>> keys = d.keys()
>>> d.update({4: 'e'})
>>> keys
dict_keys([1, 2, 3, 4])
```

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\): 

* Documentation &gt; Glossary &gt; [dictionary view](https://docs.python.org/3/glossary.html#term-dictionary-view)
* Documentation &gt; The Python Standard Library &gt; Built-in Types &gt; Mapping types -- dict &gt; [Dictionary view objects](https://docs.python.org/3/library/stdtypes.html#dictionary-view-objects)



