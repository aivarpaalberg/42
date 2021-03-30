# sõnastiku hõlmamine \(dictionary comprehension\)

## Tähendus

{% hint style="info" %}
kompaktne viis käitlemaks \(_to process_\) kõiki või osasid [itereeritava](itereeritav-iterable.md) elemente ja tagastamaks [sõnastik](sonastik-dictionary.md) \(dictionary\) tulemustega
{% endhint %}

## Täpsemalt

[Itereeritava](itereeritav-iterable.md) kõikide elementide käitlemine ja [sõnastiku](sonastik-dictionary.md) tagastamine: `anna täisarv võtmena ja täisarvu absoluutväärtus võtme väärtusena iga täisarvu kohta vahemikus -2..3 (v.a.)`

```python
>>> {i: abs(i) for i in range(-2, 3)}
{-2: 2, -1: 1, 0: 0, 1: 1, 2: 2}
```

[Itereeritava](itereeritav-iterable.md) osade elementide käitlemine ja [sõnastiku](sonastik-dictionary.md) tagastamine: `anna täisarv võtmena ja täisarvu absoluutväärtuse võtme väärtusena iga täisarvu kohta vahemikus -2..3 (v.a.) mis on paaris`

```python
>>> {i: abs(i) for i in range(-2, 3) if i % 2 == 0}
{-2: 2, 0: 0, 2: 2}
```

## Viited 

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [dictionary comprehension](https://docs.python.org/3/glossary.html#term-dictionary-comprehension)

