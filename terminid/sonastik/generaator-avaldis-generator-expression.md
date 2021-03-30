# generaator avaldis \(generator expression\)

## Tähendus

{% hint style="info" %}
[Avaldis](avaldis-expression.md) \(expression\) mis tagastab [iteraatori](iteraator-iterator.md)
{% endhint %}

## Täpsemalt

Generaator avaldis näeb välja nagu tavaline [avaldis](avaldis-expression.md) \(_expression_\). Kui loendi hõlmamisel \(_list comprehension_\) on avaldis ümbritsetud nurksulgudega \(`[]`  _brackets_\) siis generaator avaldis on ümbritsetud sulgudega \(`()`  _paranthesis_\) 

```python
>>> nums = (i * i for i in range(1, 6))  # generaator avaldis loob iteraatori 
>>> sum(nums)                            # iteraatori kasutamine
55
>>> sum(nums)                            # iteraator on ammendunud (exhausted)
0
>>> sum(i * i for i in range(1, 6))      # generaator avaldise kasutamine otse
55
```

Vaata ka [generaator](generaator-generator.md) \(_generator_\), [generaator iteraator](generaator-iteraator-generator-iterator.md) \(_generator iterator_\), [iteraator](iteraator-iterator.md) \(_iterator_\)

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [generator expression](https://docs.python.org/3/glossary.html#term-generator-expression)

