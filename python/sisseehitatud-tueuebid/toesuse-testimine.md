# Tõesuse testimine

Iga [objekti](../../terminid/sonastik/objekt-object.md) tõesust saab testida ja seda saab kasutada _if_ või _for_ tingimuses või [operandina](../../terminid/sonastik/operand-operand.md) \(_operand_\) [Boole'i tehetes](../../terminid/sonastik/boolei-tehe.md) \(_boolean operation_\)

[Objekti](../../terminid/sonastik/objekt-object.md) loetakse vaikimisi tõeseks \(_true_\).

Sisemised objektid mida tõesuse testimisel loetakse vääraks \(_false_\):

* konstandid mis on defineeritud olema väärad: `None`ja `False`
* mistahes numbritüübi null: `0`, `0.0`, `0j`, `Decimal(0)`, `Fraction(0, 1)`
* tühjad jadad \(_sequences_\) ja kogumikud \(_collections_\): `''`, `()`, `[]`, `{}`, `set()`, `range(0)`

[Tehted](../../terminid/sonastik/tehe-operation.md) \(_operations_\) ja sisseehitatud funktsioonid mis annavad tulemuseks tõesusväärtuse \(_Boolean result_\) tagastavad alati `0`või `False` väära korral ja `1` või `True` tõese korral, kui ei ole teisiti öeldud. Oluline erand: [Boole'i tehted](../../terminid/sonastik/boolei-tehe.md) \(Boolean operations\) `or` ja `and` tagastavad alati ühe operandidest.

