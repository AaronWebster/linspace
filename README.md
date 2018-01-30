% linspace, a GNU bc command line based version of the matlab/octave linspace

`linspace` prints linearly spaced values of numbers to the console:

~~~~{.bash }
localhost $ linspace
usage: linspace <min> <max> <samples> [precision]

localhost $ linspace
0
.11111111111111111111
.22222222222222222222
.33333333333333333333
.44444444444444444444
.55555555555555555556
.66666666666666666667
.77777777777777777778
.88888888888888888889
1.00000000000000000000
~~~~

For example `linspace a b N` prints $N$ samples from a to b, inclusive, with
spacing $(b-a)/(N-1)$.

This is almost identical to the matlab/octave linspace function, but with two
key differences:

* `linspace` uses GNU `bc`, which should be available on every UNIX
	system without bothering with paths, libraries, compiling, etc.
* `linspace` has many digits.

It can also take `bc` style syntax as arguments:

~~~~{.bash }
localhost $ linspace s\(0\) \(3+5\)/4 10
0
.22222222222222222222
.44444444444444444444
.66666666666666666667
.88888888888888888889
1.11111111111111111111
1.33333333333333333333
1.55555555555555555556
1.77777777777777777778
2.00000000000000000000
~~~~

To install, put it somewhere in your `$PATH` (e.g. `$HOME/bin`).


