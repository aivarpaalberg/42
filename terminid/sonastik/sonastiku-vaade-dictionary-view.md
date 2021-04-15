# sõnastiku vaade \(dictionary view\)

## Tähendus

{% hint style="info" %}
[objekt](objekt-object.md) \(_objekt_\) mida tagastavad `dict.keys()`, `dict.values()`ja `dict.items()`
{% endhint %}

## Täpsemalt

Sõnastiku vaate objektid pakuvad \(_provide_\) sõnastiku kirjete \(_dictionary's entries_\) dünaamilist vaadet \(_dynamic view_\) mis tähendab, et kui [sõnastik](sonastik-dictionary.md) muutub siis vaade peegeldab neid muutusi. Sundimaks \(_to force_\) sõnastiku vaadet muutuma [loendiks](loend-list.md) \(_list_\) kasuta `list(dictview)` 

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



