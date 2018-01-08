## inf-crystal.el
*Run a Inferior-Crystal process in a buffer -*- lexical-binding: t; -*-*

---
[![License GPLv3](https://img.shields.io/badge/license-GPL_v3-green.svg)](http://www.gnu.org/licenses/gpl-3.0.html)

inf-crystal provides a REPL buffer connected
to a [icr](https://github.com/crystal-community/icr) subprocess.

It's based on ideas from the popular `inferior-lisp` package.

`inf-crystal` has two components - a basic crystal REPL
and a minor mode (`inf-crystal-minor-mode`), which
extends `crystal-mode` with commands to evaluate forms directly in the
REPL.

`inf-crystal` provides a set of essential features for interactive
Crystal development:

* REPL
* Interactive code evaluation

### ICR

To be able to connect to [inf-crystal](https://github.com/brantou/inf-crystal.el),
you need to make sure that [icr](https://github.com/crystal-community/icr) is installed.
Installation instructions can be found on
the main page of [icr](https://github.com/crystal-community/icr#installation).

### Installation

#### Via package.el

TODO

#### Manual

If you're installing manually, you'll need to:
* drop the file somewhere on your load path (perhaps ~/.emacs.d)
* Add the following lines to your .emacs file:

```elisp
   (autoload 'inf-crystal "inf-crystal" "Run an inferior Crystal process" t)
   (add-hook 'crystal-mode-hook 'inf-crystal-minor-mode)
```

### Usage

Run one of the predefined interactive functions.

See [Function Documentation](#function-documentation) for details.


### Function Documentation


#### `(inf-crystal-reset)`

Clear out all of the accumulated commands.

#### `(inf-crystal-toggle-debug-mode)`

Toggle debug mode off and on.
In debug mode icr will print the code before executing it.

#### `(inf-crystal-enable-paste-mode)`

Enable paste mode.

#### `(inf-crystal-disable-paste-mode)`

Disable paste mode.

#### `(inf-crystal-clear-repl-buffer)`

Clear the REPL buffer.

#### `(inf-crystal-quit &optional BUFFER)`

Kill the REPL buffer and its underlying process.

You can pass the target BUFFER as an optional parameter
to suppress the usage of the target buffer discovery logic.

#### `(inf-crystal-restart &optional BUFFER)`

Restart the REPL buffer and its underlying process.

You can pass the target BUFFER as an optional parameter
to suppress the usage of the target buffer discovery logic.

#### `(inf-crystal CMD)`

Launch a crystal interpreter in a buffer.
using ‘inf-crystal-interpreter’as an inferior mode.

Argument CMD defaults to ‘inf-crystal-interpreter’.
When called interactively with ‘prefix-arg’, it allows
the user to edit such value.

<!-- Error: (wrong-number-of-arguments function 2) -->

<!-- Error: (wrong-number-of-arguments function 2) -->

<!-- Error: (wrong-number-of-arguments function 2) -->

#### `(crystal-send-last-sexp)`

Send the previous sexp to the inferior crystal process.

#### `(crystal-send-line)`

Send the current line to the inferior crystal process.

#### `(crystal-send-definition)`

Send the current definition to the inferior crystal process.

#### `(crystal-send-definition-and-go)`

Send the current definition to the inferior Crystal.
Then switch to the process buffer.

#### `(crystal-send-region START END)`

Send the region delimited by START and END to inferior crystal process.

#### `(crystal-send-region-and-go START END)`

Send the region delimited by START and END to inferior crystal process.
Then switch to the process buffer.

#### `(crystal-send-buffer)`

Send the current buffer to the inferior crystal process.

#### `(crystal-send-buffer-and-go)`

Send the current buffer to the inferior crystal process.
Then switch to the process buffer.

-----
<div style="padding-top:15px;color: #d0d0d0;">
Markdown README file generated by
<a href="https://github.com/mgalgs/make-readme-markdown">make-readme-markdown.el</a>
</div>
