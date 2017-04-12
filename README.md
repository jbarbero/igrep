igrep
-----

igrep is a convenient, caching wrapper around tesseract that lets you search through the text of your images quickly. It works on Linux and OS X, and should work on any BSDs that have a modern bash.

Installation
------------
1. Install tesseract
2. Copy or symlink igrep and progressbar anywhere in your PATH

Usage
-----

    Usage: igrep [OPTIONS] PATTERN FILE ...

    Searches inside text of images using tesseract, caches results by
    file contents.

    Options:
        -t | --threads NUM      Number of threads, default 10
        --timing                Print timing information

    The following options are passed directly to grep without interpretation:
        -A NUM                  (grep) Print NUM lines of context after
        -B NUM                  (grep) Print NUM lines of context before
        -C NUM                  (grep) Print NUM lines of context before and after
        -c                      (grep) Print number of matches only
        --colour WHEN           (grep) Use colour WHEN: {always|never|auto}
        -E                      (grep) Use extended regular expressions
        -F                      (grep) Use fixed string patterns
        -G                      (grep) Use basic regular expressions
        -i                      (grep) Use case-insensitive searches
        -m NUM                  (grep) Stop searching after NUM matches
        -v                      (grep) Invert match sense
        -w                      (grep) Match pattern only at word boundaries
        -x                      (grep) Match entire line

Known issues
------------
- I haven't implemented getopt, so you can't combine multiple options into one
- Files with same names assumed to be same content, this will be fixed later
- Progress bar broken on GNU
