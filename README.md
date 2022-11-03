# NaNoGenMo 2022
For NaNoGenMo 2022, I will use GPT-2 to generate a philosophy treatise written by a drunk, rambling philosopher.

The process for this is as follows:
1. Finetune GPT-2 on philosophy texts written by Aristotle, Plato, Kant, Hume, and Nietzsche. These texts can be found in the `corpus` folder and have been combined into a single `combined.txt` file. Finetuning is performed using the wonderful [aitextgen](https://github.com/minimaxir/aitextgen) library. 
2. Use [pytracery](https://github.com/aparrish/pytracery) to define grammars for GPT-2 prompts.
3. Use the [aitextgen](https://github.com/minimaxir/aitextgen) library to generate text. The application randomly decides whether to continue the previous text by using the last complete sentence as a prompt or to create a new paragraph with a fresh prompt generated using [pytracery](https://github.com/aparrish/pytracery). The final incomplete sentences of each generated passage is removed using [spacy](https://github.com/explosion/spaCy).
