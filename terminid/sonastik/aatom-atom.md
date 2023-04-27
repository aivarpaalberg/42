---
description: mõiste aatom (atom) määratlus (definition)
---

# aatom (atom)

**Kehtivuspiirkond** (_scope_)**:** Python

aatomid on Pythoni [avaldiste](avaldis-expression.md) (_expressions_) elementaarüksused (_most basic elements_)

## Täpsemalt

Kõige lihtsamad aatomid on [identifikaatorid](identifikaator-identifier.md) (_identifiers_) või [literaalid](literaal-literal.md) (_literals_). Sulgudes (`( )` _parentheses_), nurksulgudes (`[ ]` _brackets_) ja loogelistes sulgudes (`{ }` _braces_) olevaid vorme liigitatakse (_categorized_) süntaktilisteks aatomiteks.

```python
atom      ::= identifier | literal | enclosure
enclosure ::= parenth_form | list_display | dict_display | set_display
              | generator_expression | yield_atom
```

Seotud mõiste: [lekseem (lexical token)](lekseem-lexical-token.md)

## Viited

Pythoni ametlik dokumentatsioon (inglise keeles):

* The Python Language Reference > 6. Expressions > [6.2. Atoms](https://docs.python.org/3/reference/expressions.html#atoms)
