ac-sly
======

Emacs auto-complete for [SLY Common Lisp IDE](https://github.com/capitaomorte/sly "sly"). This is straightforward clone of
excellent [ac-slime](https://github.com/purcell/ac-slime "ac-slime") module where all "slime" words have been replaced with "sly" word. It works (for me at least).

## Setup

Install via [MELPA](http://melpa.org/#/ac-sly), or alternatively do 
the following in your `~/.emacs` or `~/.emacs.d/init/el` init file.

```elisp
(add-to-list 'load-path "/path/to/ac-sly")
(require 'ac-sly)
```

In either case add this to the init file as well:

```elisp
(add-hook 'sly-mode-hook 'set-up-sly-ac)
(eval-after-load 'auto-complete
  '(add-to-list 'ac-modes 'sly-mrepl-mode))
```
