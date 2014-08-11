utidylib
========

[![Build Status](https://travis-ci.org/nijel/utidylib.svg?branch=master)](https://travis-ci.org/nijel/utidylib)
[![Coverage Status](https://coveralls.io/repos/nijel/utidylib/badge.png?branch=master)](https://coveralls.io/r/nijel/utidylib?branch=master)
[![Code Health](https://landscape.io/github/nijel/utidylib/master/landscape.png)](https://landscape.io/github/nijel/utidylib/master)

NOTE: This repository contains a patched version of uTidyLib which
includes all Debian patches and works with Mac OS X.

This is uTidylib, the Python wrapper for the HTML cleaning
library named TidyLib: http://tidy.sf.net .  Python 2.3 or later
is required to use uTidylib.  Repeat, Python 2.3 or later is
*required* to use uTidylib.

Once installed, there are two ways to get help.  The simplest is:

    $ python
    >>> import tidy
    >>> help(tidy)
    . . .

Then, of course, there's the epydoc-generated API documentation, which
is available at site-packages/tidy/apidoc/index.html .

10 Second Tutorial
------------------

    >>> import tidy
    >>> options = dict(output_xhtml=1, add_xml_decl=1, indent=1, tidy_mark=0)
    >>> print tidy.parseString('<Html>Hello Tidy!', **options)
    <?xml version="1.0" encoding="us-ascii"?>
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml">
      <head>
        <title></title>
      </head>
      <body>
        Hello Tidy!
      </body>
    </html


Good luck!