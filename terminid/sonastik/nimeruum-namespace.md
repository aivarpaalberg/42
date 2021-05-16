# nimeruum \(namespace\)

## Tähendus

{% hint style="info" %}
koht kus muutuja \(_variable_\) on [talletatud](talletama-to-store.md) \(_stored_\). 
{% endhint %}

## Täpsemalt

Nimeruumid \(_namespaces_\) on teostatud \(_implemented_\) kui [sõnastikud ](sonastik-dictionary.md)\(_dictionaries_\). On lokaalsed \(_local_\), globaalsed \(_global_\) ja sisemised \(_built-in_\) nimeruumid ja ka pesastatud \(_nested_\) nimeruumid [objektides](objekt-object.md) \([meetodites](meetod-method.md)\).

Nimeruumid toetavad modulaarsust \(_modularity_\) ennetades nimetamise \(_naming_\) konflikte. Näiteks funktsioonid `builtins.open` ja `os.open()` on eristatavad nende nimeruumidega. Nimeruumid aitavad ka loetavust \(_readability_\) ja hooldatavust \(_maintainability_\) näidates selgelt milline moodul funktsiooni rakendab . Näiteks kirjutades `random.seed()`või `itertools.islice()`on selge, et need funktsioonid on rakendatud vastavalt `random` ja `itertools` moodulite poolt. 

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documenation &gt; Glossary &gt; [namespace](https://docs.python.org/3/glossary.html#term-namespace)

