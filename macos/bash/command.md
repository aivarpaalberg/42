# command

`command` on sisemine (_built-in_) program [täitmaks](../../terminid/sonastik/taeitmine-execution.md) (_execute_) lihtsat käsku (_simple command_) või [kuvamaks](../../terminid/sonastik/kuva-display.md) (_display_) infot käskude (_command_) kohta.

`command` jooksutab (_runs_) argumentidega käsku, summutades (_surpressing_) käsurea interpretaatori (_shell_) funktsiooni otsingut (_function lookup_) või [kuvab](../../terminid/sonastik/kuva-display.md) (_display_) informatsiooni määratletud käsu (_command_) kohta.&#x20;

Saab kasutada kettal olevate käskude aktiveerimiseks (_invoke_) kui eksisteerib samanimeline funktsioon.

Valikud:

<table><thead><tr><th>Argument</th><th>Tähendus</th><th data-hidden></th></tr></thead><tbody><tr><td>-p</td><td>kasuta vaikimisi tee (<em>PATH</em>) väärtust, mis garanteeritult leiab kõik standard utiliidid (<em>utilities</em>)</td><td></td></tr><tr><td>-v</td><td>väljasta (<em>print</em>) käsu (<em>command</em>) kirjeldus sarnaselt sisemisele käsul <code>type</code></td><td></td></tr><tr><td>-V</td><td>väljasta (<em>print</em>) paljusõnalisem (<em>more verbose</em>) kirjeldus iga käsu (<em>command</em>) kohta</td><td></td></tr></tbody></table>

&#x20;

### Näide

Kasutades bashi tuleb aeg-ajal ette, et on vaja luua uus kataloog (_directory_). Selleks saab kasutada sisemist (_built-in_) käsku  `mkdir` (_make directories_). Tihti kaasneb kataloogi loomisega vajadus sellesse ka koheselt navigeerida (nt failide loomiseks vms). `mkdir` sellist funktsionaalsust ei paku, seetõttu tuleb kõigepealt luua uus kataloog (_directory_) kasutades `mkdir` ja seejärel sellesse navigeerida kasutades teist sisemist käsku `cd` (_change directory_):

```bash
+ > pwd
/Users/aivarpaalberg/Documents
+ > mkdir test_directory # loome uue kataloogi
+ > pwd
/Users/aivarpaalberg/Documents # oleme ikka samas kataloogis
+ > cd test_directory   # navigeerime uude kataloogi
+ > pwd
/Users/aivarpaalberg/Documents/test_directory
```

Kui me seda piisavalt oleme teinud, siis võib tekkida soov asju optimiseerida: `mkdir` võiks vaikimisi luue uue kataloogi ja sellesse ka navigeerida, samas jääks vajadusel võimalus luua kataloog ilma sellesse navigeerimata (`mkdir` algne funktsionaalsus).

Soovitava eesmärgi saavutamiseks võib kirjutada lihtsa funktsiooni, mis loob uue kataloogi ja seejärel navigeerib sellesse:

```bash
function mkdir  {
    command mkdir $1 && command cd $1
  }
```

Kuna ümberkehtestame `mkdir` siis ilma  `command`  käsuta tekiks lõpmatu rekursioon (mkdir kutsuks iseennast välja). `cd` puhul pole see tingimata vajalik, vaid lihtsalt ettevaatusabinõu, et saaksime alati sisemise `cd` ja mitte võimaliku ümberkehtestatud funktsiooni.

Kasutades nüüd `mkdir` loome uue kausta ja navigeerime automaatselt sellesse kausta. Juhul, kui meil on vaja algse funktsionaalsusega sisemist  (_builtin_) `mkdir`siis kasutame `command`&#x20;

```bash
+ > pwd
/Users/aivarpaalberg/Documents
+ > mkdir test_directory # loome uue kataloogi ja navigeerime sellesse
+ > pwd
/Users/aivarpaalberg/Documents/test_directory
+ > command mkdir test_inside_test  # loome uue kataloogi ilma sellesse navigeerimata
+ > pwd
/Users/aivarpaalberg/Documents/test_directory
+ > ls
test_inside_test      
```

Saame kasutada `command` käsku  argumendiga `-V` väljastamaks paljusõnalist infot `mkdir` kohta:

```bash
+ > command -V mkdir
mkdir is a function
mkdir ()
{
    command mkdir $1 && command cd $1
}
```
