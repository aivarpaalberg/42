# generaator iteraator \(generator iterator\)

## Tähendus

{% hint style="info" %}
[objekt](objekt-object.md) mis on loodud [generaator](generaator-generator.md) funktsiooniga
{% endhint %}

## Täpsemalt

Iga `yield` peatab \(_suspends_\) ajutiselt \(_temporarily_\) käitlemise \(_processing_\), jättes meelde täitmise oleku \(_execution state_\) asukoha \(_location_\) s.h. lokaalsed muutujad \(_local variable_\) ja ootel `try` laused \(_statements_\). Kui generaator iteraator jätkab \(_resumes_\) siis jätkub see sealt kus pooleli jäi \(erinevalt funktsioonidest mis alustavad uuesti igal väljakutsel\)

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [generator iterator](https://docs.python.org/3/glossary.html#term-generator-iterator)

