# muudetav \(mutable\)

## Tähendus

{% hint style="info" %}
muudetavate [objektide](objekt-object.md) \(_mutable object_\) väärtus \(_value_\) saab muutuda kuid nad säilitavad oma [identiteedi](identiteet-identity.md) \(_identity_\)
{% endhint %}

## Täpsemalt

[Objektid](objekt-object.md) \(_object_\) mille väärtus võib muutuda öeldakse olevat **muudetavad** \(_mutable_\). Nende objektide väärtus võib muutuda kuid nende identiteet jääb samaks.

```python
>>> spam = [1, 2, 3]
>>> id(spam)
140447132656640        # objekti identiteet konkreetses arvutis
>>> spam.append(4)
>>> spam
[1, 2, 3, 4]
>>> id(spam)
140447132656640        # peale muutmist on identiteet sama
```

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentationd &gt; Glossary &gt; [mutable](https://docs.python.org/3/glossary.html#term-mutable)
* Documentation &gt; The Python Language Reference &gt; 3. Data model &gt;  [3.1. Objects, values and types](https://docs.python.org/3/reference/datamodel.html#objects-values-and-types)



