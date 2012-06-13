A simple VTE-based terminal.

Termite looks for ``termite.cfg`` in ``$XDG_CONFIG_HOME`` (or ``~/.config`` if
unset) and then falls back to ``$XDG_CONFIG_DIRS``.

DEPENDENCIES
============

A vte version >= 0.30.

DEFAULT KEYBINDINGS
===================

* ``Control+Shift+Escape``: reload configuration file
* ``Control+Shift+c``: copy to CLIPBOARD
* ``Control+Shift+v``: paste from CLIPBOARD
* ``Control+Shift+u``: unicode input (standard GTK binding)
* ``Control+Shift+f``: start forward search
* ``Control+Shift+b``: start reverse search
* ``Control+Shift+j``: start forward url search
* ``Control+Shift+k``: start reverse url search
* ``Control+Shift+n``: jump to next search match
* ``Control+Shift+p``: jump to previous search match
* ``Control+Tab``: start scrollback completion

During scrollback search, the current selection is changed to the search match
and copied to the PRIMARY clipboard buffer.

With the scrollback completion/widget open, up/down cycle through completions,
escape closes the widget and enter accepts the input.

TODO
====

* tab and shift-tab bindings for completion
* better url matching regex
* hint mode overlay for urls (like elinks/vimperator/pentadactyl)
* scrollback search needs to be improved upstream [1]_
* expose more options in ``termite.cfg``, including keybindings

.. [1] https://bugzilla.gnome.org/show_bug.cgi?id=627886
