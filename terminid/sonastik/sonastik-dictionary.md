# sõnastik \(dictionary\)

## Tähendus

{% hint style="info" %}
Pythoni sisemine \(_built-in_\) [andmetüüp](andmetueuep-datatype.md) \(_data type_\), assotsiatiivne massiiv \(_associative array_\) kus suvalised \(_arbitrary_\) võtmed on vastendatud \(mapped\) väärtustega
{% endhint %}

## Täpsemalt

Teistes programmeerimiskeeltes kutsutakse seda mõnikord paisk \(_hash_\) või paisketabel \(_hash map_\), kuigi see on tehniliselt eksitav, sest paiskadresseerimine \(_hashing_\) on üks viis teostada \(_implement_\) assotsiatiivset massiivi \(_associative array_\) kuid mitte ainuke. 

Sõnastike \(_dict_\) kasutamine on sarnane loenditele \(_list_\), kuid võtmeteks \(_keys_\) võib olla mistahes objekt paiskefunktsiooniga ja mitte ainult täisarvud \(_integers_\) alustades nullist.

```python
>>> dict_ = {'eesnimi': 'John', 'perenimi': 'Cleese'} # sõnastik (dict)
>>> dict_['eesnimi']                                  # võtmeks sõne
'John'
>>> list_ = ['John', 'Cleese']                    # loend (list)
>>> list_[0]                                      # ainult täisarv indeksid
'John'
```

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [dictionary](https://docs.python.org/3/glossary.html#term-dictionary)

