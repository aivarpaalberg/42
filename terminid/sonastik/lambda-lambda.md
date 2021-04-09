# lambda \(lambda\)

## Tähendus

{% hint style="info" %}
anonüümne reasisene \(_inline_\) [funktsioon](funktsioon-function.md) mis koosneb ainsast \(_single_\) [avaldisest](avaldis-expression.md) \(_expression_\) mida hinnatakse \(_evaluated_\)  siis kui funktsioon välja kutsutakse.
{% endhint %}

## Täpsemalt

Lambda funktsiooni loomise süntaks on: `lambda [parameetrid]: avaldis` 

Sünktaktiliselt \(_syntactically_\) on `lambda` funktsioon piiratud \(_restricted_\) ainsa avaldisega \(_single expression_\). Semantiliselt \(_semantically_\) on see aga vaid tavalise funktsiooni defineerimise süntaktiline suhkur \(_synctactic suger_\). Nii nagu pesastatult defineeritud funktsioonid \(_nested function definitions_\) saavad ka lambda funktsioonid viidata \(_reference_\) muutujaid \(_variables_\) sisalduvast käsitlusalast \(_containing scope_\).

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [lambda](https://docs.python.org/3/glossary.html#term-lambda)
* Documentation &gt; The Python Language Reference &gt; 6. Expressions &gt; [6.14. Lambdas](https://docs.python.org/3/reference/expressions.html#lambda)
* Documentation &gt; The Python Tutorial &gt; 4. More Control Flow Tools &gt; 4.7. More on Defining Functions &gt; [4.7.6. Lambda expressions](https://docs.python.org/3/tutorial/controlflow.html#lambda-expressions)
* Documentation &gt; Python HOWTOs &gt; Functional Programming HOWTO &gt; [Small functions and lambda expressions](https://docs.python.org/3/howto/functional.html#small-functions-and-the-lambda-expression)
* Documentation &gt; Python Frequently Asked Questions &gt; Design and History FAQ &gt; [Why can't lambda expressions contain statements?](https://docs.python.org/3/faq/design.html#why-can-t-lambda-expressions-contain-statements)

