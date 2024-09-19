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

Don't hard-code numbers like 5... but it's someone else's code??

```cpp
    for (i = 0; i < 5; i++) {
        for (j = 0; j < 5; j++) {
```

[Test a user's expectations](https://github.com/code-craft-us-1/test-failer-in-cpp-srivathsa-sarvothama/blob/58f95872c35183e18fcbbee37ac27a7c8530d8bf/misaligned/ColorPairTests.cpp) of the manual

[Prefer specific types](https://github.com/code-craft-us-1/test-failer-in-cpp-srivathsa-sarvothama/blob/58f95872c35183e18fcbbee37ac27a7c8530d8bf/tshirts/TShirtSize.cpp) for 'mistake proofing'

[Test with the smallest possible data](https://github.com/code-craft-us-1/test-failer-in-cpp-jayydev/blob/4a7e84398cff86862f3231b7ff42ac4281358704/misaligned.cpp)

[Test samples](https://github.com/code-craft-us-1/test-failer-in-cpp-Karan-Dutt/blob/4948075e6bebca4c22c443f8b1b11122d069e92e/TestFailer/UnitTests/src/testColorCombinations.cpp)

[Automate the test](https://github.com/code-craft-us-1/test-failer-in-cpp-ashankkumarsingh/blob/51ec2cf4978a5042a4b725df44a644b7e42da1c9/misaligned.cpp#L104) for "alignment"

