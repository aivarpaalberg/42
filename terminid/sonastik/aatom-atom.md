---
description: aatomid on Pythoni avaldiste (expressions) algelemendid (most basic elements).
---

# aatom \(atom\)

Kõige lihtsamad aatomid on [identifikaatorid](https://notebooks.azure.com/perfringo/projects/python/html/terminid/identifikaator.ipynb) \(identifiers\) või [literaalid](literaal-literal.md) \(literals\). Sulgudes \(`( )` _parentheses_\), nurksulgudes \(`[ ]` _brackets_\) ja loogelistes sulgudes \(`{ }` _braces_\) olevaid vorme liigitatakse \(_categorized_\) süntaktilisteks aatomiteks.

```python
atom ::= identifier | literal | enclosure
enclosure ::= parenth_form | list_display | dict_display | set_display | generator_expression | yield_atom
```

### Viited

* [The Python Language Reference &gt;&gt;&gt; 6. Expressions &gt;&gt;&gt; 6.2. Atoms](https://docs.python.org/3/reference/expressions.html#atoms)
* [avaldis \(expression\)](avaldis-expression.md)
