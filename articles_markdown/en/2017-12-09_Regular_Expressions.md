## Regular expressions (regex, regexes, regexen) ##

Today let's dive into the topic of regular expressions, and more specifically, the PCRE (PERL Compliant Regular Expressions) flavour. It's a C regex library used by PHP, Apache, and many more languages and projects. For more informations, you can see [pcre.org](https://pcre.org/ "pcre.org") and the wikipedia article about it [wikipedia: PCRE](https://en.wikipedia.org/wiki/Perl_Compatible_Regular_Expressions "Wikipedia: PCRE").

### Regular Expression in Computer Science ###

If you want to know the difference between PCRE and the strict definition of Regular expression defined in computer science, you can go see the article on wikipedia [Regular expression](https://en.wikipedia.org/wiki/Regular_expression), more specifically [this section](https://en.wikipedia.org/wiki/Regular_expression#Patterns_for_non-regular_languages).

### What is it? ###

A regular expression is a sequence of character that define a search pattern, used to find, or find and replace text. More simply, it's a terse way to write text search like:

> Search for all words containing the letter **a** 
> 
> Search for all the words that are not containing the letter **b**
>
> Search for all words beginning by the letter **a**
>
> Search for all words ending by a number

### Basics ###

Let's start by the beginning. We said we define a pattern to find some text. For example, I want to find a word containing the letter **a**. The regex is simply **/a/** (in PCRE you must include delimiter to open and close your expression, here I used **/**. More on that later).   

You can see the result [here](https://regex101.com/r/hJYGGz/1/)

On the linked page, you can see that if the pattern is **/a/** , you match words containing lowercase **a** but not uppercase **A**. Pattern matching is case sensitive by default, you can change that behavior with flags (More on that later).

### Ressources to learn ###
- [regex101.com](https://regex101.com/) is a place where you can test your regexes live. It support many flavour of regex, explain step by step what the regex you wrote is supposed to do, and contains also a documentation explaining many features existing for many flavour of regexes. Try it out, it works very well! 
- TODO
- TODO

### Links ###
- [https://en.wikipedia.org/wiki/Perl_Compatible_Regular_Expressions](https://en.wikipedia.org/wiki/Perl_Compatible_Regular_Expressions)
- [https://pcre.org](https://pcre.org)
- [stackoverflow](https://stackoverflow.com/questions/tagged/regex)