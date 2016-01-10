
# go-sugar

Go is "missing" a lot of the syntactic sugar that I appreciated in languages
like Python and Scala. Most of what I have read suggests I should give it time
and it will start to feel natural.  The Golang authors have often rejected
proposals which add this syntactic sugar to the core library.

This repo tracks the things I feel are missing. Maybe everyone is right, and
eventually I won't miss these niceties, or maybe eventually I'll turn this into
a library to provide them.


## Maps

    Keys(m map[T]interface{}) []T
    Values(m map[interface{}]T) []T
    Items(m map[T]U) []PairTU
    FromKVString(kvs []string) map[string]string

## Arrays

    Contains(seq []T) bool
    IndexOf(item T, seq []T) int

## Iteration

    Map(f func(item T) U, seq []T) []U
    Filter(f func(item T) bool, seq []T) []T
    Reduce(f func(item T) U, seq []T, initial *U) U
    Flatten(seq [][]T) []T
    FlatMap(f func(item T) []U, seq []T) []U

## Channels

    Drain(c chan T) []T
    Fill(seq []T) chan T


## Related

A list of related projects. `gen` looks very promising. It provides some of this
(although uses C# naming instead of the more familiar Python/Scala naming). It
may at least provide a mechanism for creating this.

* http://clipperhouse.github.io/gen/
* https://github.com/cheekybits/genny (inactive? no commits in almost a year)
* http://bouk.co/blog/idiomatic-generics-in-go/ (cool idea, but alpha)
* https://github.com/go-goast/goast
* https://github.com/reusee/ccg
* https://github.com/ncw/gotemplate
* https://github.com/joeshaw/gengen
* http://blog.ralch.com/tutorial/golang-code-generation-and-generics/
