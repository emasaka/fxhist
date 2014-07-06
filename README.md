# fxhist

Print Firefox histories from command line

## SYNOPSIS

    fxhist [-h] [--e PATTERN ...] N

## DESCRIPTION

Prints URLs that recent accessed by Firefox.

* __N:__ number of URLs (required).
* __-e PATTERN, --excludeurl PATTERN:__ exclude URLs which matches to _PATTERN_.
  _PATTERN_ is treated as LIKE pattern in SQL.

## LIMITATION

* Supports only Linux desktop
* Runs on Python 2.x

## EXAMPLES

Select URL by [percol](https://github.com/mooz/percol) and open it.

    fxhist --excludeurl %mail.google.com% 100 | percol | sed 's/.* //' | xargs xdg-open

## AUTHOR

emasaka
