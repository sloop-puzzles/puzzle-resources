# Puzzle-Resources

List of puzzle resources we use  

## Google Sheets Specific

### [puzzlehunt-discordbot](https://github.com/sloop-puzzles/puzzlehunt-discordbot)
This is our puzzle discord bot, huntbot. It's a fork of [Ladder Dog's Bot](https://github.com/azjps/ladder_dogs_discord_bot) but with a couple additional features that fit our team. But we use it to manage team communication and automatic spreadsheet creation for pretty much all of the hunts we do. 

### [mystery-hunt-sheets-addons](https://github.com/sloop-puzzles/mystery-hunt-sheets-addons)
Aother fork with some useful functions to use in googlesheets. We manually add this to the google sheet created by huntbot but one day I (kristen) will make this just work I swear. The functions are pretty well documented, if you wanted to know what's there, read the code ¯\_(ツ)_/¯.

## Grid puzzles 

### [grilops](hhttps://obijywk.github.io/)
Grilops is a grid puzzle logic sovler library based on z3. It's pretty powerful, the examples include a lot of the really common constraint/Nikolai style puzzle types. Often it is really just faster to do the puzzle yourself but i've used it to write solvers in a couple hunts. (or just used the examples provided as just to have a solver for certain puzzle types I don't feel like doing myself). Z3 on it's own is sometimes helpful too. For familiarity with using z3 in python I've found [this tutorial and reference](https://ericpony.github.io/z3py-tutorial/guide-examples.htm) particularly helpful. 

## Text/Word Matching

### [Nutrimatic](https://nutrimatic.org/)
We all know it, we all love it. Nutrimatic. Pattern matcher of champions, uses both dictionary and wikipedia phrases for pattern matching. Gold standard for things that might be real phrases. Not as great for complex patterns or single words/strict dictionary match. Can be slow. 

### [Qat](https://www.quinapalus.com/cgi-bin/qat)
While nutrimatic is the gold standard for pattern matching phrases, Qat is your bet bet for word and dictionary matching. You can really think of qat as pattern matcher meets constraint solver, extremely powerful for finding single word matches and sets of words that match given constraints. Unlike solver tools or Nutrimatic, it only does dictionary matching so you can not match phrases (unless you know the word breaks then you could treat each word in a phrase as a single word, but don't expect that to have the same contextual value as something like nutrimatic) 
For a fun way to really get to know the inner workings of qat, I recommend this puzzle from QoDe hunt [Qatalog](https://ona.quest/puzzle/qatalog)

### [Solver tools](https://github.com/sloop-puzzles/solvertools)
This technically has more things than just pattern matching but it mostly is. It has a bunch of tools for anagramming, pattern matching and some other puzzle specific stuff (`brute_force_diagonalize`, `index_all_the_things`). I primarily use `search` which is fairly similar to nutrimatic. Since everything local with a indexed wordlist on your machine, its a lot faster so especially with longer final answers and/or a lot of missing data (Metas with like 20 character answers), this tool works decently well when nutrimatic might be chuggin along. I usually keep this loaded in python repl incase it comes in handy. 

