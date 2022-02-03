---
title: "Code Review Emoji Guide"
date: 2022-02-03T11:12:05-06:00
draft: false
---

A simple emoji legend to help convey intention and added meaning in code review
comments.

I've found that while reviewing code; that emoji's lend themselves well to
providing context at a glance when there is shared understanding of their
intention. Often when I come into a new work environment; as the new person on
staff I'm uncertain what the behavior characteristics are of my reviewer. I'll
spend cycles trying to fix a stray comment that later is mentioned to be "out of
scope". This could be avoided with a simple "out of scope" prefix in the comment
so I'm aware of the intent of the reviewer; but that's not always something I
can count on.

Thus; I've taken some time to think through how to provide context with a simple
emoji table, so I can prefix a comment with one - and link to this guide as part
of my closing comments when doing code review.

## Emoji Legend

|        | `:code:`                         | Meaning                                                                                                                                                                                                                                         |
| :-:    | :----------:                     | -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------                                                             |
| 😃👍💯 | `:smiley:` `:+1:` `:100:`        | I like this... <br /><br /> ...and I want the author to know it! This is a way to highlight positive parts of a code review.                                                                                                                    |
| 🔧     | `:wrench:`                       | I think this needs to be changed. <br /><br />This is a concern or suggested change/refactor that I feel is worth addressing.                                                                                                                   |
| ❓     | `:question:`                     | I have a question. <br /><br /> This should be a fully formed question with sufficient information and context that requires a response.                                                                                                        |
| 🤔💭   | `:thinking:` `:thought_balloon:` | Let me think out loud here for a minute. <br /><br /> I might express concern, suggest an alternative solution, or walk through the code in my own words to make sure I understand.                                                             |
| 🌱     | `:seedling:`                     | Planting a seed for future. <br /><br /> An observation or suggestion that is not a change request, but may have larger implications. Generally something to keep in mind for the future.                                                       |
| 📝     | `:memo:`                         | This is an explanatory note, fun fact, or relevant commentary that does not require any action.                                                                                                                                                 |
| ⛏      | `:pick:`                         | This is a nitpick. <br /><br /> This does not require any changes and is often better left unsaid. This may include stylistic, formatting, or organization suggestions and should likely be prevented/enforced by linting if they really matter |
| ♻️      | `:recycle:`                      | Suggestion for refactoring. <br /><br /> Should include enough context to be actionable and not be considered a nitpick.                                                                                                                        |
| 🏕     | `:camping:`                      | Here is an opportunity, not directly related to your changes, for us to leave the campground [code] cleaner than we found it.                                                                                                                   |
| 📌     | `:pushpin:`                      | This is a concern that is _out of scope_ and should be staged appropriately for follow up.                                                                                                                                                      |

## Usage

Prepend comments with the appropriate emoji to convey the meaning associated
with it. Combine emoji for added fun/context.

## Examples

> 🔧 We have an existing package, `github.com/mycorp/corp-package`, that
> accomplishes this same task. Let's pull it in and replace your implementation
> with it.

> ♻️ This section of code feels like it could be extracted nicely into a separate
> module. I file like that would create clearer boundaries, and increase
> reusability.

> 📌 We really need to invest some time in refactoring out our use of this deprecated library. _Issue created: [LINK TO ISSUE]_.

> 🔧 ♻️ This method feels overly verbose and I can see can that we can simplify this approach by [DOING X]. I think this should be refactored before we merge this feature and this becomes a permanent pattern in our codebase.


### Credits

A lot of inspiration for this was driven by my consumption of
[gitmoji](https://github.com/carloscuesta/gitmoji/) 
