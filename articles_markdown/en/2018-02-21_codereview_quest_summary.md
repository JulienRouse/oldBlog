## CodeReview Quest summary ##

### Preamble ###
This post is a follow-up on the post I made at the start of January. It's probably better to go read it before to get the full picture (or to refresh your memory if you need it). You can read the previous post [here](www.julienrouse.com/template/articles/en/2018-01-06_StackExchange_codereview_quest.html).

### Results ###

I made **5** code reviews from January 6 to February 6:

- [A review in Python of a stack inplementation](https://codereview.stackexchange.com/a/184444/87312)
- [A review in Java of the implementation of Conway's Game of life](https://codereview.stackexchange.com/a/184519/87312)
- [A review in Java of a JavaFX program to calculate XP points for fantasy characters](https://codereview.stackexchange.com/a/185096/87312)
- [A review in Java of an algorithm to remove occurrences of items in an array](https://codereview.stackexchange.com/a/185247/87312)
- [A review in Java of a JSON schema validation helper](https://codereview.stackexchange.com/a/185423/87312)

Three of them got 0 votes, one got 3 positive votes, and one got 5 positive votes. On StackExchange, an answer is considered a top post(meaning a good post) if it reaches 5. So one of my answers qualifies for good material, one is 'OK' but not great, and three of them are considered bad or useless(most of those answers were seen by least than 50 peoples, but still nobody voted for it).

### Reflection on those reviews ###

For Python, it's been quite some time I haven't done anything meaningful so I did review the style of the code and   I wrote a little paragraph on `self` in Python and its use and differences with Java `this`. I should probably code more in Python before reviewing more code, unless beginner's code. It forced me to look up **PEP** documents about styling code in Python, namely [**PEP8**](https://www.python.org/dev/peps/pep-0008/) which is the official style guide on Python, and [**PEP257**](https://www.python.org/dev/peps/pep-0257/) which is the official style guide on documentation. Those **PEP** documents are more about convention than strict laws, nevertheless those conventions are really well respected in Python and should be known.

Overall this review in Python reminded me some good practices, but mostly that I am out of practice in Python and need to code again seriously with it before trying to help others. (Unless on basic stuff, or non-language dependent concepts).

As for Java, I have mixed feelings. In those reviews, I spotted bad naming, code that could be refactored, good and bad uses of `Exception`, bad uses of documentation/comments. But other answers provided insights that I did miss like a better way of solving the problem, when there was too much (useless) comments, and also post that were maybe more opinion based but that were contrary to what I wrote. It means a few things: sometimes, coding is opinion based, which is fine. Also I need to try to take a step back and look at the problem in the big picture, not to miss when problem can be solved more efficiently by changing the overall way of doing it, instead of trying to improve locally a suboptimal way of solving a problem.

Reading Java code again and trying to understand and improve on it was hard, I'll start to practice soon again to get better at it.

### Conclusion ###

It was a good experience reading other people code, I should definitely do it again to keep improving my reviewing skill. 

If you read it all, Yeah! You should definitely try as well the code review experience on [codereview](https://codereview.stackexchange.com/).