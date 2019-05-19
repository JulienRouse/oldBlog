## Start of a new ClojureScript project ##

The last few weeks I have been busy starting a new project in ClojureScript. I've played my fair share of minigames on websites like [Kongregate](https://www.kongregate.com/), [Armor Games](https://armorgames.com/) or more recently HTML5 games on [itch.io](https://itch.io/).

I set my mind to build a little [Idle game](https://en.wikipedia.org/wiki/Incremental_game) (or incremental game). It's a project I had already done a little 1 week prototype last summer with AngularJS, and I wanted to start again with Clojure/ClojureScript and [reagent](https://github.com/reagent-project/reagent)  ([reagent useful doc](https://github.com/reagent-project/reagent/tree/master/docs)), a binding library for React.

 - [Klispe](https://github.com/viebel/klipse)
 
To write my little prototype, and to not have the burden of installing a new dev environment for this little project, I found [klispe](https://github.com/viebel/klipse) which is a client-side code evaluator pluggable on any web page. It supports a lots of language like Python, Ruby, C++, Scheme, Clojure/ClojureScript (the one I used in my project) and many more languages.

To make it work, you have to paste a little snippet of Javascript inside your webpage and  then you have the REPL experience inside your HTML page. How cool is that? :) 

 - The project
 
For now I have a very early prototype, lacking a lot of content but that show a bit how the game might turn out. It would needs a rewrite to have a cleaner code base, some tests, documentation and adding a lots of content.

The step to build it were:
 
1. Start very small with just one "building" producing a fixed amount per click.
2. Add a timer to get an income coming in every second.
3. Add another "building", and update the function in charge of calculating income.
4. Add upgrades (which are income multiplier you buy)
5. Add saving/resetting the game with browser cookies.
6. Upgrade the UI (it's not very good right now but still 1000X better than what it was for most of the project).
7. Add a bit of content to see if everything works.

Working with a REPL and seeing the result on the same page was a great way of prototyping this project. (Although Klispe began to show it's limit once the project got into the three digits lines of code.)

### What's next ###

 I'm gonna rewrite/fix some of the issues on this project but this time I set up a nice dev environment

- [Emacs/Cider](https://github.com/clojure-emacs/cider)
- [reagent](https://github.com/reagent-project/reagent)  ([reagent useful doc](https://github.com/reagent-project/reagent/tree/master/docs))
- [lein-figwheel](https://github.com/bhauman/lein-figwheel)
- [cljs.test](https://clojurescript.org/tools/testing)

Some other interestings libraries I might want to use for this project (or a new one) are:

- [reframe](https://github.com/Day8/re-frame) re-frame is a pattern for writing SPAs in ClojureScript, using Reagent.
- [test.check](https://github.com/clojure/test.check) (and a wrapper for it [test.chuck](https://github.com/gfredericks/test.chuck)) which is inspired by the very good Haskell library QuickCheck. (to do some properties testing)

### The prototype ###

Below you can play with the early prototype.