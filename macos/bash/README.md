# bash



MacOS toetab sisselogimise skripte (_login scripts_) ja keskkonna omaduste loendeid (_environment property lists_) mis lubavad määrata keskkonna muutujaid (_environment variables_) ja aliaseid (_alias_)  mis jõustatakse (_set_)  automaatselt uue kesta (_shell_) jooksutamisel (_run_).

Bourne kest (_shell_) (bash, zsh jne):

Püsivate (_persistently_) keskkonna muutujate (_environment variables_)  seadmiseks ja aliaste kehtestamiseks saab neid lisata järgmistesse failidesse:

* &#x20;`~/.profile` - [täidetakse ](../../terminid/sonastik/taeitmine-execution.md)(_executed_) automaatselt kõigi sisselogitavate kestade (_login shells_) korral
* `~/.bash_profile` - sarnane `.profile` aga täidetakse ainult bash sisselogitava kesta korral (_bash login shell_).
* &#x20;`~/.bashrc` (ja  \~/.zshrc) täidetakse automaatselt kõigi `bash` (või `zhs`) mitte-sisselogitavate (_non-login_) kestade korral s.t. kui kirjutada käsureal `bash` või kui jooksutada (_run_) skripti mis algab `#!/bin/bash`&#x20;

Kasulik võib olla .bashrc fail mis (_sources_) .profile faili:

```bash
​. $HOME/.profile
```



