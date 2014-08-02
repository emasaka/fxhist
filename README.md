# fxhist

Print Firefox histories from command line

## SYNOPSIS

    fxhist [-h] [-d] [-e PATTERN ...] N

## DESCRIPTION

Prints URLs that recent accessed by Firefox.

* __N:__ number of URLs (required).
* __-e PATTERN, --excludeurl PATTERN:__ exclude URLs which matches to _PATTERN_.
  _PATTERN_ is treated as LIKE pattern in SQL.
* __-d, --dedupe:__ dedupe results.

## LIMITATION

* Supports only Linux desktop
* Runs on Python 2.x

## EXAMPLES

Select URLs by [percol](https://github.com/mooz/percol) and open it.

    $ fxhist -d -e %mail.google.com% 100 | percol | sed 's/.* //' | xargs -n 1 xdg-open

## AUTHOR

emasaka
