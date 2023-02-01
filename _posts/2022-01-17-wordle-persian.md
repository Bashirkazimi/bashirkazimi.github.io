---
layout: post
title: Wordle in Persian
date: 2022-01-17
description: I created a Persian version of the popular Wordle game.
disqus_comments: true
---

Update
======

- I added more words from [Datasets for Farsi (Persian) Natural Language Processing (NLP)](https://nlpdataset.ir/){:target="_blank"} into the game.


Wordle in Persian
======

[Wordle](https://www.powerlanguage.co.uk/wordle/){:target="_blank"}, which has recently become popular, is a seemingly simple but difficult game. The goal is for the player to guess a randomly selected five-letter solution word in 6 tries. At each try, each cell in the 6x5 grid in the game changes color depending on the inserted characters by the player. A cell turns green if the corresponding letter is part of the solution word and in the correct spot. It turns yellow if the letter is in the solution word but not at the correct spot. It turns gray if the letter is not part of the solution at all. At the end of the game (after 6 tries), the now colored grid is shown to the user indicating how they performed.

Inspired by the open-source [code](https://github.com/hannahcode/wordle){:target="_blank"} by [Hannah Park](https://www.hannahmariepark.com/){:target="_blank"}, I created a Persian version of the game. I used the [Dari Dataset for Part-of-Speech](https://depositonce.tu-berlin.de/handle/11303/11536){:target="_blank"} to select 5-letter words tagged as *Noun* to be included in the game. So, don't be disappointed if you guess a proper 5-letter Persian word and the game tells you the word does not exist :D It just means the word was not included in the game.

While the original [Wordle](https://www.powerlanguage.co.uk/wordle/){:target="_blank"} has a single word everyday for everyone, this version here lets you play as many times as you want and everyone gets a different random word every time they play.

Here is the link to the [Github repo](https://github.com/Bashirkazimi/wordle-persian){:target="_blank"}. The game is deployed on netlify [here](https://zealous-varahamihira-36b0cb.netlify.app/){:target="_blank"}. I hope you enjoy playing. 

Please let me know if you see any mistakes or have any questions/suggestions. You could also follow me on [Twitter](https://twitter.com/bashir_kazimi){:target="_blank"} and [LinkedIn](https://www.linkedin.com/in/bashirkazimi/){:target="_blank"}.

Thanks for reading!