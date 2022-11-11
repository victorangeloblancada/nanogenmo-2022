# NaNoGenMo 2022
For NaNoGenMo 2022, I will use GPT-2 to generate a philosophy treatise written by a drunk, rambling philosopher.

The process for this is as follows:
1. Finetune GPT-2 on philosophy texts written by Aristotle, Plato, Kant, Hume, and Nietzsche. These texts can be found in the [corpus](https://github.com/victorangeloblancada/nanogenmo-2022/tree/main/corpus) folder and have been combined into a single [combined.txt](https://github.com/victorangeloblancada/nanogenmo-2022/blob/main/corpus/combined.txt) file. Finetuning is performed using the wonderful [aitextgen](https://github.com/minimaxir/aitextgen) library. aitextgen and the finetuning notebook used were developed by [Max Woolf](https://github.com/minimaxir). The finetuning notebook can be found on Colab [here](https://colab.research.google.com/drive/15qBZx5y9rdaQSyWpsreMDnTiZ5IlN0zD?usp=sharing). The finetuned model is stored in the `trained_model_philosophy` folder. Unfortunately, the finetuned model is too big to be saved on GitHub.
2. Use [pytracery](https://github.com/aparrish/pytracery) to define grammars for GPT-2 prompts.
3. Use the [GPT-Philosophy.ipynb](https://github.com/victorangeloblancada/nanogenmo-2022/blob/main/GPT-Philosophy.ipynb) notebook to generate text using the aitextgen library. The application randomly decides whether to continue the previous text by using the last complete sentence as a prompt or to create a new paragraph with a fresh prompt generated using pytracery. The final incomplete sentences of each generated passage are removed using [spacy](https://github.com/explosion/spaCy). This notebook saves its output novel to [story_philosophy.txt](https://github.com/victorangeloblancada/nanogenmo-2022/blob/main/story_philosophy.txt).

Here are some brief, cherry-picked snippets from the output:

*On loneliness:*

> What is the worst way to be lonely? Is there not a cry of distress?
>
> Certainly not.
>
> And would you then say that sorrow is the greatest good?
>
> Certainly not.
>
> And would you say that it is the greatest good, and that sorrow is the greatest evil?
>
> There would not be the heaviest thing, or the heaviest thing, if you were able to express this to yourself, as I do for the sake of the multitude; and do you not say that sorrow is the greatest good? or would you say that sorrow is the greatest evil?

*On so-called honest tyrants:*

> What if a tyrant is honest?
> 
> And if a tyrant is good for himself, if he asks what has happened to him?
>
> And that is what you say.
>
> And that is what you say?
>
> When, what is it, or why is he to be a tyrant?
>
> Because, as I do, he who is a tyrant, has the power of the law,  can be the judge of the law.
>
> And that is the reason why no one can be justly called a tyrant.
>
> And is not this the law which bids one to be a tyrant?
>
> And is not the law which bids one to be a legislator or ruler of all things?
>
> Yes, that is what they say.

*On the supposed craziness of death:*
> Why is it crazy to be dead?
>
> Certainly.
>
> What?
>
> And it is a state of mind which requires of itself and of the soul; and yet it is not a state of mind which requires the whole?
>
> Certainly.
>
> And will it not be a state of mind which requires neither the whole or parts?
>
> Certainly.
>
> And will it be the whole which requires neither parts nor parts?
>
> No, certainly not.
>
> And is it not the whole or parts which require neither parts nor parts?
>
> No, certainly not.
