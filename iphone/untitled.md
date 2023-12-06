---
description: Kuidas teha iPhone helinaid kasutas Mac arvutit
---

# Oma helinate tegemine

Helinate tegemine iPhone jaoks on lihtne kui on olemas macOS operatsioonisüsteemiga arvuti ning oled valmis kasutama terminali.

macOS sisemise (_built-in_) program **afconvert**  abil .mp3 failist .m4r (helin) tegemiseks tuleb [viibale](../terminid/sonastik/viip-prompt.md) (_prompt_) sisestada:

```bash
afconvert -f m4af -d aac helifail.mp3 minu_helin.m4r
```

helifail.mp3 asemel kirjuta oma faili tegelik nimi ja minu\_helin.m4r soovitav helina nimi (see saab iPhones helina nimeks).

Viibale sisestamisel peab olema samas kaustas kus asub helifail või andma helifaili koos teega (_path_).

Helina iPhone saamiseks tuleb telefon ühendada arvutiga, klõpsata Finderis telefonil ning olles "General" sakil lohistada helina fail selle peale. Helina fail ilmub iPhones "Ringtones" alla.

