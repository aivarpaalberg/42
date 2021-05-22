---
description: 'Staatus: mustand'
---

# Koodi silumine \(debugging\)

Olenemata programmeerimisoskuse tasemest leiad ennast aegajalt olukorrast kus  Sinu [kood](terminid/sonastik/kood-code.md) \(_code_\) annab oodatust erineva tulemus. Seda juhtub nii siis, kui Sa oled alles alustamas, aga ka siis kui oled juba programeerimises vana kala. See on täiesti normaalne. Vea võib teha \(ja teebki\) iga programmeerija ja mistahes [kodeerimise](terminid/sonastik/kodeerimine-coding.md) käigus.

## Terminoloogia

Kui [kood](terminid/sonastik/kood-code.md) annab oodatust erineva tulemuse siis öeldakse, et selles on [viga](terminid/sonastik/viga-error.md) \(_error_\). Vigade eemaldamise protsessi nimetatakse [silumiseks](terminid/sonastik/siluma-to-debug.md) \(_debugging_\).

## Vigade liigitamine

Vigade avaldumise korral aitab vigade liigitamine lihtsamini kindlaks teha kohti kus viga otsida ja leida.

Vigu võib klassifitseerida ajaperioodi järgi millal need avalduvad ja vigade tüübi alusel.

Vead võivad avalduda:

* [kompileerimise](terminid/sonastik/kompileerima-to-compile.md) ajal \(_compile time_\) 
* [käitusjärgu](terminid/sonastik/kaeitusjaerk-runtime.md) ajal \(_runtime_\)

Koodi käivitades kompileerib Python selle \(_soruce code_\) masinkoodiks \(_machine code_\). Kui teisendamine masinkoodi ei õnnestu, siis koodi ei käivitata ja Python informeerib kasutajat veast. Kompileerimise ajal kõige sagedamini esinev viga on `SyntaxError` s.t. et on eksitud süntaksi reeglite vastu. Näiteks kui kasutatakse samaliigilisi jutumärke pesastatult ilma paomärgita:

```python
>>> 'Selle raamatu kirjastaja on 0'Reilly'
  File "<stdin>", line 1
    'Seller raamatu kirjastaja on O'Reilly'
                                         ^
SyntaxError: invalid syntax
```

Kui koodis on [viga](terminid/sonastik/viga-error.md) \(_error_\) siis võib selle põhjused jagada kolmeks:

* süntaktilised vead
* semantilised vead
* loogikavead



Enimlevinud ja paljude arvates ka kõige lihtsam viis [koodi](terminid/sonastik/kood-code.md) silumiseks on Pythoni sisemise funktsiooni `print` kasutamine. Kui [programm](terminid/sonastik/programm-program.md) ei anna oodatud tulemust, siis väljastatakse võimalikes probleemkohtades objektide väärtused, et veenduda kas need on ikka need mida oodatakse. 

Kasutades [silumise](terminid/sonastik/siluma-to-debug.md) \(_debugging_\) vahendeid on võimalik vaadelda \(_examine_\) [programmi](terminid/sonastik/programm-program.md) seisundit \(_state_\), vaadata kuidas muutuvad \(oluliste\) muutujate väärtused ja isegi muuta jooksvalt muutujate väärtusi.

