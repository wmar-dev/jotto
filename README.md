# Code Breaking Games

Mastermind, Jotto, Bulls and cows, and Wordle all fall under the class of code breaking games. I like these problem, because they indicate a pratical application of information theory and information retrival. Making a best guess is based on information theory.

Entropy in information theory is defined as

$ H(X) = -\sum_{x \in X} p(x) \log p(x) $

Use log base 2 if you want to find how many bits it will take to encode the probability distributions.

In the case of information retrival, you can think the clue that is given in each round as the score when trying to find the most relevant document. 

## Ngrams

Generate 5-gram wordlist from https://norvig.com/ngrams/.

```bash
cat word.list enable1.txt TWL06.txt sowpods.txt | awk '{print tolower($0)}' | awk 'length() == 5' | sort | uniq | xz > 5-gram.txt.xz
xzcat 5-gram.txt.xz | less
```

## References
- [Entropy (information theory)](https://en.wikipedia.org/wiki/Entropy_(information_theory))
- [Bulls and cows](https://en.wikipedia.org/wiki/Bulls_and_cows)
- [Jotto](https://en.wikipedia.org/wiki/Jotto)
- [Mastermind (board game)](https://en.wikipedia.org/wiki/Mastermind_(board_game))
- [Wordle](https://en.wikipedia.org/wiki/Wordle)
- [Information Theory and the Game of JOTTO](https://dspace.mit.edu/handle/1721.1/6192)