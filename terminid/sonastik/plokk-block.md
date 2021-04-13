# plokk \(block\)

{% hint style="info" %}
Osa \(_piece_\) Pythoni programmi tekstis mida [täidetakse](taeitmine-execution.md) \(_executed_\) kui terviküksust \(_unit_\) 
{% endhint %}

 Python program is constructed from code blocks. A _block_ is a piece of Python program text that is executed as a unit. The following are blocks: a module, a function body, and a class definition. Each command typed interactively is a block. A script file \(a file given as standard input to the interpreter or specified as a command line argument to the interpreter\) is a code block. A script command \(a command specified on the interpreter command line with the [`-c`](https://docs.python.org/3/using/cmdline.html#cmdoption-c) option\) is a code block. A module run as a top level script \(as module `__main__`\) from the command line using a [`-m`](https://docs.python.org/3/using/cmdline.html#cmdoption-m) argument is also a code block. The string argument passed to the built-in functions [`eval()`](https://docs.python.org/3/library/functions.html#eval) and [`exec()`](https://docs.python.org/3/library/functions.html#exec) is a code block.

A code block is executed in an _execution frame_. A frame contains some administrative information \(used for debugging\) and determines where and how execution continues after the code block’s execution has completed.

