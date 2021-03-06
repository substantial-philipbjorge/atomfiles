# Substantial's Atom Config

## Installation instructions

If you don't have it already, [download the Atom editor](https://atom.io/)


```bash
cd ~
# If you have an atom config already:
mv .atom .atom-bak
git clone git@github.com:substantial/atomfiles.git .atom
cd .atom && bin/update-packages
```

## Goal

This is an experiment. We want to see if we can build a config that we enjoy that we all feel comfortable and productive in. Currently only a few of us have opted in, but please join and start contributing if you are interested.

## Tenets

* Tenets should be agreed upon, discussed, modified or removed if they do not fit.
* This config should be usable by all disciplines and all skill levels. It should be approachable enough for all, but powerful enough for power users.
* There is no owner. All at Substantial have an equal say in what goes in it.
* No forks, we should all run off of master. It's ok to use branches to experiment with things.
* Performance is an important part of the experience and should not be neglected. Poorly performing addons should be optimized or removed.
* No Vim mode. No Emacs mode. It is good to take inspiration from them, but we should see if we can build something as usable for all without that as a wholesale starting point. [Readline](http://www.catonmat.net/download/readline-emacs-editing-mode-cheat-sheet.pdf) keys are great and fine, but we should be sure to keep standard OS X arrow key movements as well.
* Avoid overriding keys common to other OS applications (like cmd+s).
* Try to avoid overriding default atom key bindings. If multiple keys are bound
  to the same thing (like cmd+t and cmd+p) it is more OK if the less common one
  is overridden.
* It is never done. It should be refined, added to  and optimized indefinitely.
* Be mindful of the fact that others use this config. If you have good reason to make huge changes, communicate them and seek advice on them. We shouldn't worry about backwards compatibility too much, but we should be mindful.

## Key Bindings

Most of the default Key Bindings are still enabled. Below are custom and particularly important key bindings.

Key | Command
--- | ---
**Window Navigation** |
&#x21E7;&#x2318;K | Focus Previous Pane
&#x21E7;&#x2318;J | Focus Next Pane
**Editing** |
&#x2318;= | Auto Indent
**Selecting Text** |
^S | Expand Region (word, inside parens, etc.)
^&#x21E7;S | Expand Region (word, inside parens, etc.)
^I ( | Select inside parentheses (works for `{[<'"`t`)
^O ( | Select around parentheses (works for `{[<'"`t`)
**Moving Around** |
&#x2325;P | Move up to next blank line (&#x21E7; to select)
&#x2325;N | Move down to next blank line (&#x21E7; to select)

## Packages

### How to install a new package

#### Via the command line

1. Install `my-new-package`:

   ```bash
   ~/.atom/bin/install-package my-new-package
   ```
2. Commit the change to `packages.txt` and pull request it.

#### Via the UI

1. Use the Install section of preferences to install a package.
2. Run:

    ```bash
    ~/.atom/bin/update-packages
    ```
3. Answer "keep" when asked about your package.
4. Commit the change to `packages.txt` and pull request it.

### How to upgrade packages

1. Use the UI to update packages.
2. Run:

    ```bash
    ~/.atom/bin/update-packages
    ```
3. Commit the changes to `package.txt` and pull request it.

### Installed

* [advanced-open-file](https://atom.io/packages/advanced-open-file) - A more
  reasonable file open with tab completion.
  * `cmd-opt-o` - Advanced Open
* [advanced-new-file](https://atom.io/packages/advanced-new-file) - A more
  reasonable new file with tab completion.
  * `cmd-opt-n` - Advanced New
* [color-picker](https://atom.io/packages/color-picker) - Adds a color picker.
  * `cmd-shift-c` - Pick Color
* [pigments](https://atom.io/packages/pigments) - Displays colors in projects
  and files.
* [Linter](https://atom.io/packages/linter) - Enable displaying lint (code
  style) warnings.
* [linter-eslint](https://atom.io/packages/linter-eslint) - Linter plugin for
  [eslint](https://atom.io/packages/linter-eslint)
* [expand-region](https://atom.io/packages/expand-region) - Expand selection to
  quotes/braces/brackets/etc.
  * `ctrl-s` - Expand selection
  * `ctrl-shift-s` - Shrink selection
  * `ctrl-i (` - Select inside parens, can use any of: `[{('"<t`
  * `ctrl-o (` - Select around parens, can use any of: `[{('"<t`
* [language-haml](https://atom.io/packages/language-haml) - HAML support
* [react](https://atom.io/packages/language-haml) - React support
* [block-travel](https://atom.io/packages/block-travel) - Move the cursor by code blocks
  * `alt-n` - Scroll down by blocks
  * `alt-p` - Scroll up by blocks
