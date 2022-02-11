# cut

`cut` on sisemine (_built-in_) programm: lõika välja valitud osad faili igast reast.

See programm on läheneb tekstile veergude vaatepunktist, s.t. et valitud osad on määratletud veergudena mis on eraldatud mingi sümboliga.

### Näited

Oletame, et meil on csv fail, kus on andmed eraldatud komadega ning milles on veerud nime, vanuse, pikkuse ja kaaluga:

```csv
Jüri,35,182,88
Mari,30,172,65
Bob,45,180,93
Alice,40,175,70
```

Väljasta esimene ja kolmas veerg:

```bash
+ > cut -d ',' -f 1,3 test_data.csv
Jüri,182
Mari,172
Bob,180
Alice,175
```

Väljasta esimene kuni komas veerg:

```bash
+ > cut -d ',' -f 1-3 test_data.csv
Jüri,35,182
Mari,30,172
Bob,45,180
Alice,40,175
```

Väljasta veerud alates teisest:

```bash
+ > cut -d ',' -f 2- test_data.csv
35,182,88
30,172,65
45,180,93
40,175,70
```
