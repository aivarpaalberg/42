# any(iterable)

## Käsk (command)

{% tabs %}
{% tab title="Lihtsalt" %}
kas vähemalt üks on [tõene](../sisseehitatud-tueuebid/toesuse-testimine.md)
{% endtab %}

{% tab title="Üksikasjalikult" %}
[tagasta](../../terminid/sonastik/tagastama-to-return.md#taehendus) True kui vähemalt üks [itereeritava](../../terminid/sonastik/itereeritav-iterable.md) (_iterable_) element on tõene (true); tagasta False kui itereeritav on tühi
{% endtab %}
{% endtabs %}

## Kasutamine

[Funktsioon](../../terminid/sonastik/funktsioon-function.md) `any()` on samaväärne (_equivalent_) alljärgnevaga:

```python
def any(iterable):
    for element in iterable:
        if element:
            return True
    return False
```

Koodist on näha, et funktsioon rakendab lühist (_short circuit_) s.t. et esimese tõese (_True_) korral tagastab funktsioon väärtuse ning järelejäänud elemente enam ei kontrollita.

### Argument

Funktsioonile tuleb välja kutsudes edastada üks [argument](../../terminid/sonastik/argument.md) mis peab olema **itereeritav** ([sõne](../sisseehitatud-tueuebid/sone-str/), [loend](../sisseehitatud-tueuebid/loend-list/), hulk, [sõnastik](../../terminid/sonastik/sonastik-dictionary.md#taehendus) vms).

Juhul kui [argumenti ](../../terminid/sonastik/argument.md#taehendus)ei edastata või edastatud argument ei ole itereeritav [seatakse erand](../../terminid/sonastik/erandit-seadma-to-raise-an-exception.md#taehendus) `TypeError`.

### Tagastatav väärtus

Funktsioon tagastab tõesusväärtuse (booli).

| Väärtus | Tingimus(ed)                                      |
| ------- | ------------------------------------------------- |
| True    | vähemalt üks itereeritava element on tõene¹       |
| False   | itereeritav on tühi või kõik elemendid on väärad¹ |

¹ vt [tõesuse testimine](../sisseehitatud-tueuebid/toesuse-testimine.md)

### Näited

Kas loendis on mõni 3-ga jaguv arv?

```python
>>> loend = [2, 5, 7, 11, 15, 20]
>>> any(num % 3 == 0 for num in loend)
True
>>> loend = [2, 5, 7, 11, 16, 20]
>>> any(num % 3 == 0 for num in loend)
False
```

### Viited

* Pythoni ametlik dokumentatsioon (inglise keeles): [any(_iterable_)](https://docs.python.org/3/library/functions.html#any)
* Pythoni interaktiivses interpretaatoris sisesta `help(any)`
