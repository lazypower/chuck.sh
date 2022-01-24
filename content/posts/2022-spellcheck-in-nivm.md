---
title: "Enabling spell check in Neovim for prose content"
date: 2022-01-24T01:25:28-06:00
draft: false
---

Without diving too deep into the details, I've noticed a growing trend in my developer workflow. Typos in commit messages. After being a `vim` user for many years, about 2 years ago I started using Visual Studio Code heavily. Now that I've changed jobs and am working in a mono-repo full time, the overhead of VSC is a bit too much to endure. I spun up a new dotfiles repo, and started configuring Neovim as my primary editor of choice. However, by default - it did nothing to save me from myself. I spell phonetically; therefore I misspell words often.

The fix for this was actually incredibly easy, neovim and even vim proper have a built-in spellchecking system; you just need to enable it and configure the primary language.


### Spellcheck Configuration

In my `init.vim`, I set the spelling dictionary to English, and prompt spellcheck to only surface 9 of the best suggestions.

```
" Set spellcheck lang
set spelllang=en
set spellsuggest=best,9

```

### Enable spellcheck for markdown and git commits

And I typically only really want this enabled when I'm writing in markdown or version control commit messages. I plug these into `augroup` so they don't get repeatedly loaded into vim.

```
" Enable spellcheck on markdown
augroup markdownSpell
  autocmd FileType markdown setlocal spell
  autocmd BufRead,BufNewFile *.md setlocal spell
augroup END

augroup gitcommitSpell
  autocmd FileType gitcommit setlocal spell
augroup END
```

Save, reload vim and when you're in these contexts, you should start seeing misspelled words highlighted in red.


