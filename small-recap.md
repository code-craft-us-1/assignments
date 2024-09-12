# Modularity recap

## File name shows the way

[Intuitive file names](https://github.com/code-craft-us-1/well-named-in-cpp-srirenukachaluvadi/pull/1/files)

[Separation](https://github.com/code-craft-us-1/well-named-in-cpp-jayydev/pull/1/files) of formatting from printing

[Separation](https://github.com/code-craft-us-1/well-named-in-cpp-nageshwariK/pull/1/files) of reading and writing

[Split using headers](https://github.com/code-craft-us-1/well-named-in-cpp-Sriranganatha1979)

[Separate folder for tests, separate file for formatting](https://github.com/code-craft-us-1/well-named-in-cpp-ArjunanPrakash/pull/1/files)

## Generic naming is a smell

Generic naming examples: `Utility`, `Manager`, `Handler`, `Helper`

Smell: Are you placing unrelated things in a single file?

Example: `GetColor...` and `GetPairNumber...` along with `PrintManual` - what would you call that file?

Does the `PrintManual` function evolve differently from the `Get...` functions?

## Reducing the effort of manual testing

Simple test - proves that it doesn't crash, and output is non-empty. Rest needs manual testing.

```cpp
std::string colorpairStr = ColorFormatter::printcolorcodes();
assert(!colorpairStr.empty());
```

[Testing the properties](https://github.com/code-craft-us-1/well-named-in-cpp-koushik-philips/blob/a176c41c7746e1e682a96498558ecacd68dfc90e/ColorTests.cpp) of the reference manual
