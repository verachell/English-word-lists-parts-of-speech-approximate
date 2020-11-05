# English-word-lists-parts-of-speech
Word lists categorized mainly by parts of speech. Parsed from public domain sources. WARNING: Not suitable for language teaching purposes.

These word lists are the result of parsing public domain sources. I put these lists together quickly for my NaNoGenMo 2020 project and they are far from accurate. For example, not all of the words classified as verbs are guaranteed to be 100% verbs; it's possible other words might be in there. Therefore **these are not suitable as resources for teaching English.** 

## What is the intended use of these word lists, since they cannot be considered accurate?
Great question! These are mainly intended for use in generative fiction such as NaNoGenMo projects. If (for example) you were to pick a random word out of the `verbs-present-tense` list, then you would be more likely to get a present tense verb than any other type of word. But it's not guaranteed that you'll get a present-tense verb, or even a verb at all. I did not have time to inspect the words one by one. If you're happy with that, then go right ahead and use the lists however you want to! 

This repository is released under the Unlicense, so you can use these word lists freely without attribution.

## What are the sources of these words?
I parsed them from the following sources:
- The `british-english` and `american-english` dictionaries from the [SCOWL/aspell package](http://wordlist.aspell.net/), which I will refer to here as the "Dictionary Words". These packages were provided in the Linux distro I use at `/usr/share/dict`. I combined these two dictionaries into one with duplicates removed; these were the source of some of the words in the lists.
- The public domain book at Project Gutenberg: [Part-of-Speech II by Grady Ward](http://www.gutenberg.org/ebooks/3203) 2002, which I will refer to here as the "Parts Of Speech Word Book". This book contains words in a word or phrase field delimted by a backslash and followed by part-of-speech field.

In both cases, I have made a good-faith attempt at removing profanity, racial slurs, and other offensive language (see credits for sources of such words), while making a point of avoiding the Scunthorpe Problem. However, there is no guarantee that all offensive language is filtered out, and where you draw the line is largely up to you and your application. The words here should NOT be considered as free of offensive language; you are responsible for applying your own filters.

## How these words were parsed
### Verbs
I obtained the past-tense verbs and present-tense verbs by grepping for 'ed' and 'ing' endings respectively from the Dictionary Words, then manually adding back irregular verbs that would have not been included in this crude screenign method. I also manually removed non-verb and non-past-tense words in the past-tense verbs (for example `screed`) by manually examining instances of words ending with 'eed'. As you can see, this method was merely an approximation of obtaining past- and present- tense verbs.

I obtained the verb infinitives from the Parts Of Speech Word Book by firstly selecting all verbs (those indicated with a V, i, or t part-of-speech code). From the result, I then excluded the words already in the past-tense and present-tense verb lists generated previously. Again, this method is a very blunt instrument, and these remaining words are not guaranteed to all be the infinitive form of the verb. 

## Credits
- `british-english` and `american-english` dictionaries from the [SCOWL/aspell package](http://wordlist.aspell.net/).
- [Part-of-Speech II by Grady Ward](http://www.gutenberg.org/ebooks/3203) 2002, at Project Gutenberg.

Words used for filtering out offensive language were sourced from the following:
1. [Banned Word List](http://www.bannedwordlist.com/)
2. [List of Ethnic Slurs](https://en.wikipedia.org/wiki/List_of_ethnic_slurs)
3. [List of Common Nouns Derived From Ethnic Group Names](https://en.wikipedia.org/wiki/List_of_common_nouns_derived_from_ethnic_group_names)
4. [List of LGBT-related slurs](https://en.wikipedia.org/wiki/List_of_LGBT-related_slurs)
5. I also filtered based on some words I thought of, many of which were not offensive per se but could be read the wrong way if put in a certain context. 

