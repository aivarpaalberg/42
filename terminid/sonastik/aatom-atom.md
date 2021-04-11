# aatom \(atom\)

## Tähendus

{% hint style="info" %}
aatomid on Pythoni [avaldiste](avaldis-expression.md) \(_expressions_\) elementaarüksused \(_most basic elements_\).
{% endhint %}

## Täpsemalt

Kõige lihtsamad aatomid on [identifikaatorid](https://notebooks.azure.com/perfringo/projects/python/html/terminid/identifikaator.ipynb) \(identifiers\) või [literaalid](literaal-literal.md) \(literals\). Sulgudes \(`( )` _parentheses_\), nurksulgudes \(`[ ]` _brackets_\) ja loogelistes sulgudes \(`{ }` _braces_\) olevaid vorme liigitatakse \(_categorized_\) süntaktilisteks aatomiteks.

```python
atom      ::= identifier | literal | enclosure
enclosure ::= parenth_form | list_display | dict_display | set_display
              | generator_expression | yield_atom
```

Vaata ka [lekseem \(lexical token\)](lekseem-lexical-token.md)

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* The Python Language Reference &gt; 6. Expressions &gt; [6.2. Atoms](https://docs.python.org/3/reference/expressions.html#atoms)

