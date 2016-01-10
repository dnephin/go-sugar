
# go-sugar

A library to provide some of the syntactic sugar that is omitted from the core
language.


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


## Links

* http://clipperhouse.github.io/gen/
* https://github.com/cheekybits/genny (inactive? no commits in almost a year)
* http://bouk.co/blog/idiomatic-generics-in-go/ (cool idea, but alpha)
* https://github.com/go-goast/goast
* https://github.com/reusee/ccg
* https://github.com/ncw/gotemplate
* https://github.com/joeshaw/gengen

* http://blog.ralch.com/tutorial/golang-code-generation-and-generics/
