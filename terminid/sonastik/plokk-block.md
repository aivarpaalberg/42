# plokk \(block\)

{% hint style="info" %}
osa \(_piece_\) Pythoni [programmi](programm-program.md) tekstist mida [täidetakse](taeitmine-execution.md) \(_executed_\) kui terviküksust \(_unit_\) 
{% endhint %}

## Täpsemalt

Pythoni [programm](programm-program.md) \(_program_\) on moodustatud \(_constructed_\)  koodi plokkidest \(_code block_\).

Järgnevad on plokid \(_blocks_\): 

* [moodul](moodul-module.md) \(_module_\), [funktsiooni](funktsioon-function.md) keha \(_function body_\) ja [klassi ](klass-class.md)definitsioon \(_class definition_\).  
* iga käsk \(_command_\) mis tipitakse interaktiivselt \(_typed interactively_\) on plokk \(_block_\). 
* skripti fail \(_script file_\) s.t. fail mis on antud kui tüüpne sisend \(_standard input_\) interpretaatorile \(_interpreter_\) või määratud \(_specified_\) kui interpretaatori \(_interpreter_\) käsurea \(_command line_\) argument on koodi plokk \(_code block_\). 
* skripti käsk \(_script command_\) s.t. käsk \(_command_\) mis on määratud \(_specified_\) interpretaatori \(_interpreter_\) käsureal \(_command line_\) `-c` valikuga \(_option_\) on koodi plokk \(_code block_\). 
* [moodul](moodul-module.md) mida käitatakse \(_run_\) kõrgeime taseme skriptina \(_top level script_\) \(kui mooduli `__main__`\) käsurealt \(_command line_\) kasutades `-m` argumenti on ka koodi plokk \(_code block_\). 
* [sõne](../../python/sisseehitatud-tueuebid/sone-str/) \(_string_\)[ tüüpi](andmetueuep-datatype.md) [argument](argument.md) mis edastatakse sisemistele funktsioonidele `eval()` ja `exec()` on koodi plokk \(_code block_\). 

Koodi plokki täidetakse \(_executed_\) täitmise kaadris \(_execution frame_\). Kaader sisaldab \(_contains_\) teatud \(_some_\) administratiivset informatsiooni \(_administrative information_\) mida kasutatakse silumiseks \(_debugging_\) ja mis määrab \(_determines_\) kus ja kuidas täitmine jätkub peale koodi ploki täitmist.

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; The Python Language Reference &gt; 4. Execution Model &gt; [4.1. Structure of a program](https://docs.python.org/3/reference/executionmodel.html#structure-of-a-program)

