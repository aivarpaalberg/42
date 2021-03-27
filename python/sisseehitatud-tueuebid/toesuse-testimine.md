# Tõesuse testimine

Iga objekti tõesust saab testida ja seda saab kasutada _if_ või _for_ tingimuses või operandina Boole'i tehetes

Objekti loetakse vaikimisi tõeseks \(_true_\).

Sisseehitatud objektid mida tõesuse testimisel loetakse vääraks \(_false_\):

* konstandid mis on defineeritud olema väärad: `None`ja `False`
* mistahes numbritüübi null: `0`, `0.0`, `0j`, `Decimal(0)`, `Fraction(0, 1)`
* tühjad jadad \(_sequences_\) ja kogumikud \(_collections_\): `''`, `()`, `[]`, `{}`, `set()`, `range(0)`

Tehted \(_operations_\) ja sisseehitatud funktsioonid mis annavad tulemuseks tõesusväärtuse \(_Boolean result_\) tagastavad alati `0`või `False` väära korral ja `1` või `True` tõese korral, kui ei ole teisiti öeldud. Oluline erand: [Boole'i tehted](../../terminid/sonastik/boolei-tehe.md) \(Boolean operations\) `or` ja `and` tagastavad alati ühe operandidest.

