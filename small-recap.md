# Modularity recap

## File name shows the way

[Intuitive file names](https://github.com/code-craft-us-1/well-named-in-cpp-srirenukachaluvadi/pull/1/files)

[Separation](https://github.com/code-craft-us-1/well-named-in-cpp-jayydev/pull/1/files) of formatting from printing

## Generic smells

Generic naming examples: `Manager`, `Handler`, `Helper`

Smell: Are you placing unrelated things in a single file?

Example: `GetColor...` and `GetPairNumber...` along with `PrintManual` - what would you call that file?

Does the `PrintManual` function evolve differently from the `Get...` functions?
