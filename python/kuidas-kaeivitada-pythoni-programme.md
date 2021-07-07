# Kuidas käivitada Pythoni programme?

Kui [programm](../terminid/sonastik/programm-program.md) \(_program_\) on valmis kirjutatud ja salvestatud siis on seda kasutamiseks vaja käivitada. Programmi käivitamine on sarnane mistahes [faili](../terminid/sonastik/fail-file.md) avamisega arvutis: me anname arvutile käsu, et ta avaks faili mingi kindla rakendusega. Graafilises kasutajaliideses on kaks levinud failide avamise viisi:

* avada rakendus ning `open` dialoogi abil avada fail programmi seest
* [klõpsata](../terminid/sonastik/klopsama-click.md) failil ning operatsioonisüsteem avab selle rakendusega, mis on seotud antud failitüübiga

Pythoni programme on mõistlik käivitada terminalist / kestast \(_terminal, shell_\). Selleks anname arvutile käsu, et ava rakendusega Python mingi fail. Selleks avame terminali ja sisestame [viibale](../terminid/sonastik/viip-prompt.md) \(_prompt_\):

```bash
> python minu_programm.py
```

Olenevalt arvuti seadistusest ja eesmärgist võib rakendus millega me programmifaili soovime avada olla `python`, `python3`, `python3.9` jms.

Oluline on kestaga \(_shell_\) olla samas [kaustas](../terminid/sonastik/kaust-folder.md) \(_folder_\) kus asub programmifail. Kui see tingimus ei ole täidetud, siis tuleb Pythonile öelda kus ta faili leida võib s.t. anda talle tee failini \(_file path_\).

Tekstiredaktorid \(_text editors_\) pakuvad tavaliselt võimalust käivitada fail ka `Run` käsuga. 

