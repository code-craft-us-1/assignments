# Test failer recap

Code once, print to any stream

```cpp
int printColorMap(std::ostream& out) {
    const char* majorColor[] = {"White", "Red", "Black", "Yellow", "Violet"};
    const char* minorColor[] = {"Blue", "Orange", "Green", "Brown", "Slate"};
    int i = 0, j = 0;
    for (i = 0; i < 5; i++) {
        for (j = 0; j < 5; j++) {
            out << i * 5 + j << " | " << majorColor[i] << " | " << minorColor[i] << "\n";
        }
    }
    return i * j;
}
```

---

[Test a user's expectations](https://github.com/code-craft-us-1/test-failer-in-cpp-srivathsa-sarvothama/blob/58f95872c35183e18fcbbee37ac27a7c8530d8bf/misaligned/ColorPairTests.cpp) of the manual

[Prefer specific types](https://github.com/code-craft-us-1/test-failer-in-cpp-srivathsa-sarvothama/blob/58f95872c35183e18fcbbee37ac27a7c8530d8bf/tshirts/TShirtSize.cpp) for 'mistake proofing'

