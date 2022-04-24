# Code Review - Week 3

For this coursework, you have been paired up with another trainee.

You are taking the role of the reviewer. Your pair will open a pull request with this code:

```javascript
// find returns the length of the longest element in the array.
function find(arr) {
    let l = arr[0];
    for (let i = 0; i < arr.length; i++) {
        const c = arr[i];
        if (c.length > l.length) {
            l = c;
        }
    }
    return l.length;
}
```

Your job is to leave review comments to help guide them towards improving the code.

You will leave some comments, they will respond to them (maybe with code changes, maybe with more questions), and you should keep iterating like this until you think the code can't be improved any more.

Before reading on, you should look at the above code, and think about what could be better about it. Write these ideas down.

## Rules of the game

1. You're not allowed to just rewrite the whole PR for them. Focus on what's wrong with the code (e.g. "I don't understand what this variable is for"), and give suggestions that your pair can implement (e.g. "Maybe we could this variable `cheese`"). Prefer asking leading questions to giving suggestions.
2. Links are great! You don't need to answer/explain everything yourself - if there's an example, or an explanation somewhere, link to it!

## How to give useful comments

1. Make sure you explain what the problem is - don't just say "This variable name is bad", explain what's wrong with it ("These two variable names are really similar so I get them confused" or "This variable name is a plural, so I thought it contained an array, but it's actually a string").

## Some problems with this code

These are ideas that may prompt comments for you to give - they are definitely not comments you should give exactly as written, they are not good comments!

### Naming

* `find` isn't a very descriptive name for the function - it doesn't really tell you what it's doing, or what it returns.
* `l` isn't a very clear name for a variable.

### Edge-cases

* What would you expect this function to do when it's passed an empty array? What happens when it is?

### Concise code

* Sometimes a [`for..of` loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) can be more clear than a regular `for` loop - read up on them, and see if you think it makes sense here.

## Better code

Here is an example of code which addresses all of the above problems and ideas. Your goal isn't to get to exactly this code, but something similar to it.

Notice how one of our improvements is adding a comment before the function - comments are code too, and they can be really useful and important!

```javascript
// find returns the length of the longest element in the array.
// If no elements are present, undefined will be returned.
function findLengthOfLongestElement(arr) {
    let longest = arr[0];
    for (const current of arr) {
        if (current.length > longest.length) {
            longest = current;
        }
    }
    if (longest === undefined) {
        return undefined;
    }
    return longest.length;
}
```
