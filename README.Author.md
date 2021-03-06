# Code Review - Week 3

For this coursework, you have been paired up with another trainee.

You are taking the role of the author - you are going to send some code to a reviewer, and get feedback. Your job is to respond to the feedback.

You are allowed to respond to the feedback by editing the code and updating the pull request, by responding to their comments (either with follow-up questions, or by discussing why you think the comment shouldn't be addressed), or by asking your education buddy for advice.

Read the following code (which returns the length of the longest element in an array), and make sure you understand how it works. Feel free to add some `console.log` lines after it and try running it, to make sure you're really happy you understand it.

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

Open a pull request creating a file called `code.js` containing the above code.

Assign your pair as a reviewer (TODO: Do trainees have permission to do this? This could probably be automated with some kind of GitHub bot...), and send them a link on slack to make sure they've seen it.

Keep iterating on the code, responding to their comments, until you're both happy the code can't be improved more.

## Rules of the game

You are allowed to write whatever code you think makes sense, Google as much as you want, and talk to people about the code. You can ask any questions you want, and you're allowed to disagree (but always explain why). Just like in real life, you don't need to have it all in your head - coding is a collaborative experience, and research and experimentation are great.

Use the "Assignee" field to show who's meant to be doing something. When you've sent code or comments to the revewier, remove yourself as the "Assignee" and assign your reviewer. When you're not listed as the "Assignee", you're not expected to be changing things (otherwise things can get confusing, when you update things while the other person is still reviewing). (TODO: Link to cheat-sheet entry)

## How long to spend

You are expected to spend 1-2 hours on this exercise this week as part of your coursework. This probably looks like responding to 2-5 rounds of review comments. If you think you're done after fewer than three rounds of review, reach out to your education buddy for advice on what else could be improved.
