# plokk \(block\)

## Tähendus

{% tabs %}
{% tab title="Python" %}
{% hint style="info" %}
osa \(_piece_\) Pythoni [programmi](programm-program.md) \(_program_\) [tekstist](tekst-text.md) \(_text_\) mida [täidetakse](taeitmine-execution.md) \(_executed_\) kui terviküksust \(_unit_\) 
{% endhint %}

Tihti kasutatakse sünonüümina **koodi plokk**.

## Täpsemalt

Pythoni [programm](programm-program.md) \(_program_\) on moodustatud \(_constructed_\)  koodi plokkidest \(_code block_\).

Järgnevad on plokid \(_blocks_\): 

* [moodul](moodul-module.md) \(_module_\), [funktsiooni](funktsioon-function.md) keha \(_function body_\) ja [klassi ](klass-class.md)definitsioon \(_class definition_\).  
* iga käsk \(_command_\) mis tipitakse interaktiivselt \(_typed interactively_\) on plokk \(_block_\). 
* skripti fail \(_script file_\) s.t. [fail](fail-file.md) mis on antud kui tüüpne sisend \(_standard input_\) [interpretaatorile](interpretaator-interpreter.md) \(_interpreter_\) või määratud \(_specified_\) kui interpretaatori \(_interpreter_\) käsurea \(_command line_\) argument on koodi plokk \(_code block_\). 
* skripti käsk \(_script command_\) s.t. käsk \(_command_\) mis on määratud \(_specified_\) interpretaatori \(_interpreter_\) käsureal \(_command line_\) `-c` valikuga \(_option_\) on koodi plokk \(_code block_\). 
* [moodul](moodul-module.md) mida käitatakse \(_run_\) kõrgeime taseme skriptina \(_top level script_\) \(kui mooduli `__main__`\) käsurealt \(_command line_\) kasutades `-m` argumenti on ka koodi plokk \(_code block_\). 
* [sõne](../../python/sisseehitatud-tueuebid/sone-str/) \(_string_\)[ tüüpi](andmetueuep-datatype.md) [argument](argument.md) mis edastatakse sisemistele funktsioonidele `eval()` ja `exec()` on koodi plokk \(_code block_\). 

Koodi plokki [täidetakse](taeitmine-execution.md) \(_executed_\) täitmise kaadris \(_execution frame_\). Kaader sisaldab \(_contains_\) teatud \(_some_\) administratiivset informatsiooni \(_administrative information_\) mida kasutatakse [silumiseks](siluma-to-debug.md) \(_debugging_\) ja mis määrab \(_determines_\) kus ja kuidas täitmine jätkub peale koodi ploki täitmist.
{% endtab %}

{% tab title="Andmekorraldus" %}
{% hint style="info" %}
terviküksusena \(_as a unit_\) registreeritav \(_recorded_\) või edastatav \(_transmitted_\) elemendijärjend \(_sequence of elements_\).
{% endhint %}

Elemendid \(_elements_\) võivad olla [märgid](maerk-character.md) \(_characters_\), [sõnad](sona-word.md) \(_words_\) või kirjed \(_records_\).
{% endtab %}

{% tab title="Tekstitöötlus" %}
{% hint style="info" %}
[kasutaja](kasutaja-user.md) \(_user_\) määratud \(_defined_\) [teksti](tekst-text.md) \(_text_\) katkend \(_segment_\), millele rakendatakse mingit [tekstitöötluse](tekstitoeoetlus-text-processing.md) \(_text processing_\) operatsiooni.
{% endhint %}
{% endtab %}
{% endtabs %}

## Viited

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; The Python Language Reference &gt; 4. Execution Model &gt; [4.1. Structure of a program](https://docs.python.org/3/reference/executionmodel.html#structure-of-a-program)

[EVS-ISO 2382-4:1999](https://www.evs.ee/et/evs-iso-2382-4-1999),  Infotehnoloogia. Sõnastik. Osa 4: Andmekorraldus

* [plokk \(_block_\)](https://www.eki.ee/dict/its/index.cgi?Q=D08C91DC-6C03-1014-88DC-FC5F0DBED45A&F=GUID&C01=1&C02=0&C10=1)

[EVS-ISO/IEC 2382-23:1998](https://www.evs.ee/et/evs-iso-iec-2382-23-1998), Infotehnoloogia. Sõnastik. Osa 23: Tekstitöötlus

* [plokk \(_block_\)](https://www.eki.ee/dict/its/index.cgi?Q=D4DD4AB8-6C03-1014-88DC-FC5F0DBED45A&F=GUID&C01=1&C02=0&C10=1)

