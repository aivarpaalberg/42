# loendi hõlmamine \(list comprehension\)

## Tähendus

{% hint style="info" %}
kompaktne viis käitlemaks \(_to process_\) kõiki või osasid [itereeritava](itereeritav-iterable.md) elemente ja tagastamaks [loend](loend-list.md) \(_list_\) tulemustega
{% endhint %}

## Täpsemalt 

[Itereeritava](itereeritav-iterable.md) kõikide elementide käitlemine ja [loendi](loend-list.md) tagastamine: `anna mulle Unicode koodipunkt iga tähe kohta sõnes` 

```python
>>> [ord(char) for char in 'abc']
[97, 98, 99]
```

Itereeritava osade elementide käitlemine ja loendi tagastamine: `anna mulle arvu ruut iga arvu kohta ennikus mis on paarisarv`

```python
>>> [i * i for i in (3, 5, 6, 7, 8) if i % 2 == 0]
[36, 64]
```

Vaata ka [sõnastiku hõlmamine](sonastiku-holmamine-dictionary-comprehension.md) \(_dictionary comprehension_\)

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [list comprehension](https://docs.python.org/3/glossary.html#term-list-comprehension)

