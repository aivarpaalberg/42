# parameeter \(parameter\)

## Tähendus

{% hint style="info" %}
nimega [olem](olem-entity.md) \(_entity_\)  [funktsiooni](funktsioon-function.md) \(või [meetodi](meetod-method.md)\) definitsioonis mis määrab \(_specifies_\) [argumendi](argument.md) \(või argumendid\) mida funktsioon vastu võtab \(_accept_\)
{% endhint %}

## Täpsemalt

Parameetreid on viite liiki:

* **kohapõhine-või-võtmesõna**: määrab \(_specifies_\) [argumendi](argument.md) mida saab edastada \(_passed_\) kas kohapõhiselt või kui võtmesõna argumendi. See on vaikimisi parameetri liik, näiteks `bacon` ja `eggs` järgnevas:

```python
def func(bacon, eggs=None): ...
```

* **ainult kohapõhine**: määrab \(_specifies_\) [argumendi ](argument.md)mida saab edastada \(_supplied_\) ainut kohapõhiselt. Ainult kohapõhiseid parameetreid saab defineerida lisades \(_by including_\) nende järel `/` märgi \(_character_\) funktsiooni parameetrite loendisse, näiteks `pos_only1` ja `pos_only2` järgnevas:

```python
def func(pos_only1, pos_only2, /, kohapõhine_või_võtmesõna): ...
```

* **ainult võtmesõna**: määrab \(_specifies_\) [argumendi ](argument.md)mida saab edasada ainult võtmesõnaga \(_keyword_\). Ainult võtmesõna parameetreid saab defineerida lisades ühe \(_var-positional_\) parameetri või `*` märgi parameetrite loendis  

_keyword-only_: specifies an argument that can be supplied only by keyword. Keyword-only parameters can be defined by including a single var-positional parameter or bare `*` in the parameter list of the function definition before them, for example _kw\_only1_ and _kw\_only2_ in the following:

* ```text
  def func(arg, *, kw_only1, kw_only2): ...
  ```
* _var-positional_: specifies that an arbitrary sequence of positional arguments can be provided \(in addition to any positional arguments already accepted by other parameters\). Such a parameter can be defined by prepending the parameter name with `*`, for example _args_ in the following:

  ```text
  def func(*args, **kwargs): ...
  ```

* _var-keyword_: specifies that arbitrarily many keyword arguments can be provided \(in addition to any keyword arguments already accepted by other parameters\). Such a parameter can be defined by prepending the parameter name with `**`, for example _kwargs_ in the example above.

Parameters can specify both optional and required arguments, as well as default values for some optional arguments.

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [parameter](https://docs.python.org/3/glossary.html#term-parameter)

