# argument \(argument\)

## Tähendus

{% hint style="info" %}
väärtus mis edastatakse [funktsioonile](funktsioon-function.md) \(või [meetodile](meetod-method.md)\) seda välja kutsudes
{% endhint %}

## Täpsemalt

Argumente on kahte liiki:

* **võtmesõna argument** \(_keyword argument_\)- argumendid millele eelneb [identifikaator](identifikaator-identifier.md) \(`nimi=`\) [funktsiooni](funktsioon-function.md) väljakutses või edastatakse \(_passed_\) kui väärtus [sõnastikus](sonastik-dictionary.md) \(_dict_\) millele eelneb `**`. 
* **kohaargument** \(_positional argument_\) - argumendid mis ei ole võtmesõna argumendid on kohaargumendid. Kohaargumendid võivad ilmuda \(_appear_\) argumentide loendi alguses või edastatakse[ itereeritava](itereeritav-iterable.md) elementidena millele eelneb `*`. 

Argumendid omistatakse \(_assigned_\) nimega lokaalsetele muutujatele \(_local variables_\) funktsiooni kehas \(_body_\)

### Võtmesõna argument

Kui on [funktsioon](funktsioon-function.md) `summa` ja sellel on kaks võtmesõna argumenti \(_keyword argument_\): `hind` ja `kogus` siis saab seda funktsiooni välja kutsuda kahel viisil:

```python
summa(hind=4, kogus=2)        # identifikaatoritega
summa(**{hind:4, kogus:2})    # sõnastikuga
```

[Sõnastiku](sonastik-dictionary.md) saab funktsioonile edastada ka [nimena](nimi-name.md) \(_name_\):

```python
andmed = {hind: 4, kogus:2}
summa(**andmed)               # nimega sõnastikuga
```

### Kohaargument

Kui on [funktsioon](funktsioon-function.md) `summa`ja selle on kaks kohaargumenti \(_positional argument_\) siis saab seda funktsiooni välja kutsuda kahe viisil:

```python
summa(4, 2)      # kohaargumentidega
summa(*(4, 2))   # itereeritavaga
```

[Itereeritava](itereeritav-iterable.md) \(_iterable_\) saab edastada ka [nimena](nimi-name.md) \(_name_\):

```python
andmed = (4, 2)
summa(*andmed)   # nimega itereeritavaga
```

Vaata ka [parameeter](parameeter-parameter.md) \(parameter\)

### Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [argument](https://docs.python.org/3/glossary.html#term-argument)

