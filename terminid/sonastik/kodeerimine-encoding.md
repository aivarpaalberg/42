# kodeerimine \(encoding\)

## Tähendus

{% hint style="info" %}
[andmete](andmed-data.md) \(_data_\) teisendamine mingi koodi abil, näiteks teksti teisendamine baitide objektiks \(_byte object_\)
{% endhint %}

## Täpsemalt

Kodeermine \(_encoding_\) antud tähenduses ei ole andmete salastamine/krüpteerimine vaid teisendamine kuigi sageli on kodeeritud andmed inimesele loetamatud.

Näiteks saab Pythonis tekstilist andmetüüpi [sõne](../../python/sisseehitatud-tueuebid/sone-str/) \(_str_\) teisendada ehk kodeerida \(_encode_\) baitide objektiks \(_byte object_\):

```python
>>> print(*'Tere maailm!'.encode())
84 101 114 101 32 109 97 97 105 108 109 33
```

