rlgrep
------

rlgrep - grep for Ruby on Rails log files. Can grep through multiple files at once, including gzipped ones.

Usage
=====

rlgrep [options] regular_expression log files

Available options:
-c, --colorize    highlight important elements of request
-h, --help        display this help
-i pattern, --highlight=pattern
                  highlight specified pattern
-p param, --highlight-param=param
                  highlight specified param
-s file_name, --stdin=file_name
                  parse file from STDIN, display it's name as file_name
-x, --cleanup     remove session information

My Favourite Usage
==================

rlgrep -c -x -p action -i 'Rendering: [0-9\.]+' '"show"' production.log{.{3..1}.gz,} | less
