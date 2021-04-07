# sgrep

The stupid/scalable grep

## What is sgrep?
sgrep uses lex to set up and compile a custom lexer for the supplied pattern,
the result is a binary that will specifically scan for the supplied pattern.

Technically sgrep can out-perform grep given the following cases are met.

* You wish to grep a large (and I mean __really__ large file), sgrep pays the
  initial cost of setting up and compiling the lexer, but in theory gains
  performance over traditional grep. Hence sgrep will eventually catch up and
  pass grep in scanning and matching.

* You constantly search for the same pattern. Then using sgrep you pay the cost
  of building the custom lexer once, and can reuse it as many times as you
  like.

The above statements where made with rudimentary testing and observing the
results I drew the aforementioned conclusions, I plan to formally test and
prove these results.

## Disclaimer

This is a (semi) joke and I made this whilst learning how to use lex to build a
lexer for my honors projects.

## TODO

Add full grep options.
