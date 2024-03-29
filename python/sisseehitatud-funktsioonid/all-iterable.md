# all(iterable)

## Käsk (command)

{% tabs %}
{% tab title="Lihtsalt" %}
kas pole ühtegi väära
{% endtab %}

{% tab title="Üksikasjalikult" %}
[tagasta](../../terminid/sonastik/tagastama-to-return.md#taehendus) True kui [itereeritava](../../terminid/sonastik/itereeritav-iterable.md) (_iterable_) kõik elemendid on [tõesed](../sisseehitatud-tueuebid/toesuse-testimine.md) (true) või kui itereeritav on tühi.
{% endtab %}
{% endtabs %}

## Kasutamine

[Funktsioon](../../terminid/sonastik/funktsioon-function.md#taehendus) `all()`on samaväärne (_equivalent_) alljärgnevaga:

```python
def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```

[Koodist](../../terminid/sonastik/kood-code.md) on näha, et [funktsioon](../../terminid/sonastik/funktsioon-function.md) rakendab lühist (_short circuit_) s.t. et esimese väära (_False_) korral tagastab funktsioon väärtuse ning järelejäänud elemente enam ei kontrollita.

**Oluline meeles pidada**: tühjas sõne tõesusväärtus on _False_ aga _all()_ tagastab tühja itereeritava korral _True_

### Argument

Funktsioonile tuleb välja kutsudes edastada üks [argument](../../terminid/sonastik/argument.md) mis peab olema [itereeritav](../../terminid/sonastik/itereeritav-iterable.md) ([sõne](../sisseehitatud-tueuebid/sone-str/), [loend](../../terminid/sonastik/loend-list.md), hulk, [sõnastik](../../terminid/sonastik/sonastik-dictionary.md#taehendus) vms).&#x20;

Juhul kui [argumenti](../../terminid/sonastik/argument.md) ei edastata või edastatud argument ei ole [itereeritav](../../terminid/sonastik/itereeritav-iterable.md)  [seatakse erand](../../terminid/sonastik/erandit-seadma-to-raise-an-exception.md#taehendus) `TypeError`.

### Tagastatav väärtus

Funktsioon tagastab tõesusväärtuse (booli):

|  Väärtus  | Tingimus(ed)                                                                                                                |
| --------- | --------------------------------------------------------------------------------------------------------------------------- |
| **True**  | kõik[ itereeritav](../../terminid/sonastik/itereeritav-iterable.md#taehendus)a elemendid on tõesed¹ või itereeritav on tühi |
| **False** | vähemalt üks itereeritava element on väär¹                                                                                  |

¹ vt [tõesuse testimine](../sisseehitatud-tueuebid/toesuse-testimine.md)

### Näited

**Kas kõik itereeritava elemendid on tõesed?**

```python
>>> all('abc')
True
>>> all('')
True
>>> all([1, 2, 3])
True
>>> all([0, 1, 2])
False
```

**Kas kõik elemendid vastavad seatud tingimusele?**

Antud on DNA ahel ning on vaja kontrollida kas see on kehtiv s.t. selles esinevad ainult `A`, `C`, `G` või `T`&#x20;

```python
>>> ahel = 'TATCAGAAAACACGCGCTTAAGTGAGCGGAACGGGTGGAACAAGGTTGTA'
>>> lubatud = ('A', 'C', 'G', 'T')
>>> all(char in lubatud for char in ahel)
True
>>> ahel = 'TATCAGAAAACACGCGCTTAAGTGAGCGGAACGGGTGGAACAAGGUTTGTA'
>>> all(char in lubatud for char in ahel)
False
```



## Viited

* Pythoni ametlik dokumentatsioon (inglise keeles): [all(iterable)](https://docs.python.org/3/library/functions.html#all)
* Pythoni interaktiivses interpretaatoris sisesta `help(all)`
