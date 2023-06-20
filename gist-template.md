# Breakdown of a Regular Expression Hex-Code Search

This is a gist of Regular Expressions and their functions

## Summary

This is a gist breakdown of a the following regular expression including what the different operators in the following expression too.
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

In this following gist I will go over regular expression and its compenents and break them down below

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [The OR Operator](#the-or-operator)

## Regex Components

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

For the following I will be taking out the slashes and as we go along will be taking portions out as I explain them

First the slashes will contain our regex expression, you can also with constructors include quotation marks but for this example /'s contain the expression.

### Anchors

^ and $ are anchors, in basics this determines where the start and the end of a statement, for example with the following snippit: `^#?([a-f0-9]{6}|[a-f0-9]{3})$`

^ dictates the start of the search statement, this means that nothing can preceed the search, meaning ^This picks up This or This thing but "this" does not or "athis" doesn't.

The $ in the formula is the ending anchor, cutting off the rest of the search.
For example ^Hello$ in abstract would pick up "Hello" and not "HelloThere"

### Quantifiers

The Quanitifiers of this expression are the following {6} {3} and ?

What these do is dictate the amount of times a search happens, so in our code example.
#? dictates that # will be searched for once.

and [a-f0-9]is searched for {6} and {3} times respectively. For example aaa would pull correctly or a8bc45 would too.

### Grouping Constructs

Grouping constructs are pretty cut and dry, much like in mathematics () act as a sub expression to measure on.
For our example above:

The expression ([a-f0-9]{6}|[a-f0-9]{3}) is calculated in its entirety separately from the # that preceeds it.
Meaning that it will search for either of these conditions (by utilizing the OR function but we will go over that later)
And treat it as a conditional before applying the # and anchors to it.

### Bracket Expressions

In our expression we have a couple of components wrapped in brackets [], these are Bracket Expressions.
What these do is provide us a range of characters or list of characters to search off of.
So lets break down our Bracket Expression.

The following Bracket Expression is repeated twice: [a-f0-9]
Lets take the first part a-f what this doesn't do is search for the literal character, a, -, and f
but rather searches on all characters a-f in other words a,b,c,d,e, or f.

For the second portion 0-9 does the same but all digits 0,1,2,3,4,5,6,7,8,9.
So this section is searching for characters a,b,c,d,e,f,0,1,2,3,4,5,6,7,8,9.

Please note that this is case sensitive, this will not search for capital letters in this range.

### The OR Operator

The OR operator is | what this does is measure on two conditions, much like the traditional OR in a computer science conditional.

For the above expression ([a-f0-9]{6}|[a-f0-9]{3}), this statement is measuring if we can find 6 characters a-f or 0-9 in any combination, or 3 characters a-f or 0-9 in any combination. If either of these conditions are met, the search contained in the parenthesis will be met, external conditions on the outside of the parenthesis will apply separate from the OR.

## Author

My name is Alexandra Winter, at this point in time I am a 24 year old aspiring developer who loves progamming, camping, and all in all fun adventures. 
Below is the link to my GitHub Profile: 
https://github.com/AWinterCoding
