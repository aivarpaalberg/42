# loendi hõlmamine \(list comprehension\)

## Tähendus

{% hint style="info" %}
kompaktne viis käitlemaks \(_to process_\) kõiki või osasid [itereeritava](itereeritav-iterable.md) elemente ja tagastamaks [loend](loend-list.md) \(_list_\) tulemustega
{% endhint %}

## Täpsemalt 

Loendi hõlmamine \(_list comprehension_\) pakub sisutihedat \(_concise_\) viisi[ loendite](loend-list.md) \(_list_\) loomiseks. 

Tavalisteks kasutusjuhtumiteks on uue loendi loomine mille iga element on teise itereeritava iga elemendiga teostatud toimingu tulemus või ainult see osa elementidest, mis vastab teatud tingimustele.

[Itereeritava](itereeritav-iterable.md) kõikide elementide käitlemine ja [loendi](loend-list.md) tagastamine: `anna mulle Unicode koodipunkt iga märgi kohta sõnes` 

```python
>>> [ord(char) for char in 'abc']
[97, 98, 99]
```

Loendi hõlmamise süntaks võib esialgu tunduda arusaamatu, kuna element millest peale käitlemist saab  uue loodava loendi \(_list_\) element on enne `for` [silmust](silmus-loop.md) \(_loop_\). Samas on see tegelikult lihtne nagu on näha järgnevast skeemist:

```bash
     mis sa      kuskohast sa                     
      saad        selle saad                  
       │              │
  ╭────┴────╮╭────────┴────────╮
  
 [ ord(char)  for char in 'abc' ]
  
  ╰────┬────╯╰────────┬────────╯ 
       │              │          
                                
   anna mulle    iga märgi kohta                  │
    Unicode         sõnes      
   koodipunkt

```

[Itereeritava](itereeritav-iterable.md) osade elementide käitlemine ja loendi tagastamine: `anna mulle arvu ruut iga arvu kohta ennikus mis on paarisarv`

```python
>>> [i * i for i in (3, 5, 6, 7, 8) if i % 2 == 0]
[36, 64]
```

Siin on süntaks pikem kui põhimõte jääb samaks:

```python
  mis sa      kuskohast sa         mis tingimusel sa            
   saad        selle saad            selle saad      
     │               │                    │     
  ╭──┴──╮╭───────────┴────────────╮╭──────┴──────╮
  
 [ i * i  for i in (3, 5, 6, 7, 8)  if i % 2 == 0 ]
  
  ╰──┬──╯╰────────────┬───────────╯╰──────┬──────╯
     │                │                   │   
                                
   anna mulle   iga täisarvu kohta      mis on             │
   arvu ruut       ennikus            paarisarv 

```

Vaata ka [sõnastiku hõlmamine](sonastiku-holmamine-dictionary-comprehension.md) \(_dictionary comprehension_\)

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [list comprehension](https://docs.python.org/3/glossary.html#term-list-comprehension)
* Documentation &gt; The Python Tutorial &gt; 5. Data Structures &gt; 5.1. More on lists &gt; [5.1.3. List Comprehensions](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions)

