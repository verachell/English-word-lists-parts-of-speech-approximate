# English-word-lists-parts-of-speech-approximate
Word lists categorized approximately by parts of speech. Parsed from open-source lists as shown in details and sources. WARNING: Not suitable for language teaching purposes.

These word lists are the result of parsing. I put these lists together quickly for my NaNoGenMo 2020 project and they are far from accurate. For example, not all of the words classified as verbs are guaranteed to be 100% verbs; it's possible other words might be in there. Therefore **these are not suitable as resources for teaching English.** 

## What is the intended use of these word lists, since they cannot be considered accurate?
These are mainly intended for use in generative fiction such as NaNoGenMo projects. If (for example) you were to pick a random word out of the `verbs-present-tense` list, then you would be more likely to get a present tense verb than any other type of word. But it's not guaranteed that you'll get a present-tense verb, or even a verb at all. I did not have time to inspect the words one by one. If you are comfortable with those limitations, then go right ahead and use the lists however you want to! 

This repository is released under the Unlicense, so you can use these word lists freely without attribution.

## What are the sources of these words?
I parsed them from the following sources:
- The `british-english` and `american-english` dictionaries from the [SCOWL/aspell package](http://wordlist.aspell.net/), see also  which I will refer to here as the "Dictionary Words". These packages were provided in the Linux distro I use at `/usr/share/dict`. I combined these two dictionaries into one with duplicates removed; these were the source of some of the words in the lists.
- The public domain book at Project Gutenberg: [Part-of-Speech II by Grady Ward](http://www.gutenberg.org/ebooks/3203) 2002, which I will refer to here as the "Parts Of Speech Word Book". This book contains words in a word or phrase field delimted by a backslash and followed by part-of-speech field.

In both cases, I have made a good-faith attempt at removing profanity, racial slurs, and other offensive language (see credits for sources of such words), while making a point of avoiding the Scunthorpe Problem. However, there is no guarantee that all offensive language is filtered out, and where you draw the line is largely up to you and your application. The words here should NOT be considered as free of offensive language; you are responsible for applying your own filters.

## How these words were parsed
### Verbs
I obtained the **past-tense verbs** and **present-tense verbs** by grepping for 'ed' and 'ing' endings respectively from the Dictionary Words, then manually adding back irregular verbs that would have not been included in this crude screening method. I also manually removed non-verb and non-past-tense words in the past-tense verbs (for example `screed`) by manually examining instances of words ending with 'eed'. As you can see, this method was merely an approximation of obtaining past- and present- tense verbs.

I obtained the **verb infinitives** from the Parts Of Speech Word Book by firstly selecting all verbs (those indicated with a V, i, or t part-of-speech code). From the result, I then excluded the words already in the past-tense and present-tense verb lists generated previously. Again, this method is a very blunt instrument, and these remaining words are not guaranteed to all be the infinitive form of the verb. 

For the **transitive past tense** and **transitive present tense** verbs, I first selected all transitive verbs from the Parts of Speech Word Book (those indicated with a t code). As an approximation to separate the tenses, of the transitive verbs, those ending in 'ed' were selected for the past tense. Transitive verbs ending in 'ing' wwere selected for the present tense.

### Nouns
**Nouns ending with `ment`** were obtained by selecting all nouns from the Parts of Speech Word Book (those indicated with an N code), and then limiting by to those ending with 'ment'.

I obtained **Plural nouns** by selecting the plural words from the Parts of Speech Word Book (those indicated with a p code) and removing verbs and non-plural nouns by a mix of grep and of manual inspection.

**Noun phrases** were selected from the Parts of Speech Word Book (those indicated with an h code).

### Other categories
**Adverbs** were obtained by selecting adverbs from the Parts of Speech Word Book (those indicated with a v code). I manually deleted some which would not work conveniently in the place of a general adverb in generative fiction. These were words such as `yes`, `no`, `ago`, `yesterday`, and several more.

The **Interjections** were the result of selecting words in the Parts of Speech Word Book indicated by an exclation mark (!) code. I manually deleted several which would not work well on their own as interjections. In usage, these would need to have an exclamation mark appended, and would typically be used in dialogue.

**Counjunctions** were parsed by selecting words in the Parts of Speech Word Book indicated by an C code. This was a small list, so I was able to inspect all of it manually. I deleted some words that would not have worked well here or were not in common usage (e.g. `whither`).

I obtained **Prepositions** by selecting words in the Parts of Speech Word Book indicated by a P code. This was a small list, so I was able to inspect all of it manually. I deleted some words that would not have worked well in present-day fiction or were not in common usage (e.g. `ere`, `circa`).

**Adjectives** were parsed by selecting words in the Parts of Speech Word Book indicated by an A code. 

I parsed **Ly Adverbs** by grepping for 'ly' at the end of a line in the Adverbs file.

In "other categories", the file **safe-american-british-english-all-words.txt** is a list of all the American English and British English words (combined with duplicates removed) that begin with a lowercase letter, do not contain punctuation, and have been filtered for bad words as described on this page. These words make a good general-use English dictionary, however, be aware the filters used here may or may not suit your purposes.

## Credits
- `british-english` and `american-english` dictionaries from the [SCOWL/aspell package](http://wordlist.aspell.net/) via the standard Debian package manager. See also [https://metadata.ftp-master.debian.org/changelogs//main/s/scowl/scowl_7.1-1_copyright](https://metadata.ftp-master.debian.org/changelogs//main/s/scowl/scowl_7.1-1_copyright)
- [Part-of-Speech II by Grady Ward](http://www.gutenberg.org/ebooks/3203) 2002 at Project Gutenberg.

Words used for filtering out offensive language were sourced from the following:
1. [Banned Word List](http://www.bannedwordlist.com/)
2. [List of Ethnic Slurs](https://en.wikipedia.org/wiki/List_of_ethnic_slurs)
3. [List of Common Nouns Derived From Ethnic Group Names](https://en.wikipedia.org/wiki/List_of_common_nouns_derived_from_ethnic_group_names)
4. [List of LGBT-related slurs](https://en.wikipedia.org/wiki/List_of_LGBT-related_slurs)
5. I also filtered based on some words I thought of, many of which were not offensive per se but could be read the wrong way if put in a certain context. 

