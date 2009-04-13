README
======

My modifications of jEdit's
[WhiteSpace plugin](http://plugins.jedit.org/plugins/?WhiteSpace).

Currently, the only modification is the way how lines containing only
whitespace characters are displayed: instead of displaying such lines as
having leading whitespace, the lines are shown as having trailing
whitespace. This is more intuitive than the original behavior; if trailing
whitespace is configured to be shown, but leading whitespace is not,
whitespace-only lines are emphasized.

Installation
------------

The installation is essentially a hack.

Take a copy of the modified source files of the plugin to a directory. At
the root of the directory, enter

    $ ant -Djedit.install.dir=/path/to/dir/containing_jedit4.3preX.jar -Dinstall.dir=.

This will build `WhiteSpace.jar` into the current directory.

We need to know where jEdit is configured to store installed plugins. This
is either jEdit's installation directory or `~/.jedit`. From now on, we call
that directory as `$JEDIT_HOME`.

Make a backup copy of the plugin's original jar file, found in
`$JEDIT_HOME/jars` directory. Delete file
`$JEDIT_HOME/jars-cache/WhiteSpace.jar.summary`.

Replace the plugin's original jar file with the modified file.

Legal notes
-----------

Use the software at your own risk.

The software is originally copyrighted by Andre Kaplan and Nathan Jones,
released under GPLv2.
