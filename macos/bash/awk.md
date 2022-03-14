# awk

`awk` on sisemine (_built-in_) programm: mustritest juhinduv skaneerimise (_scanning_) ja töötlemise (_processing_) keel (_language_)

### Näited

Oletame, et meil on csv fail, kus on andmed eraldatud komadega ning milles on veerud nime, vanuse, pikkuse ja kaaluga:

```csv
Jüri,35,182,88
Mari,30,172,65
Bob,45,180,93
Alice,40,175,70
```

Väljasta esimene ja viimane veerg:

```bash
+ > awk -F ',' '{print $1, $NF}' test_data.csv
Jüri 88
Mari 65
Bob 93
Alice 70
```