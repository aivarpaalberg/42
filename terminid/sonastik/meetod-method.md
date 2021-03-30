# meetod \(method\)

## Tähendus

{% hint style="info" %}
[Funktsioon](funktsioon-function.md) \(_function_\) mis on defineeritud [klassi](klass-class.md) kehas \(_class body_\)
{% endhint %}

## Täpsemalt

Kui meetod kutsutakse välja selle defineerinud[ klassi](klass-class.md) eksemplaril \(_instance_\) [atribuudina](atribuut-attribute.md) \(_attribute_\) siis meetodi esimeseks [argumendiks](argument.md) \(_argument_\) saab eksemplari objekt \(_instance object_\) mida tavaliselt kutsutakse `self` .

```python
# dict klassi eksemplar
>>> d = dict(enumerate('abc', start=1))   
# meetod atribuudina dict klassi eksemplaril
>>> d.get(2)                              
'b'
# esimese argumendi (self) edastamine ilmutatult (explicitly)
>>> dict.get(d, 2)
'b'
```

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [method](https://docs.python.org/3/glossary.html#term-method)

