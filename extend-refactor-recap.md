# Recap of extending and refactoring

## Runtime language selection

[Language file with messages](https://github.com/code-craft-us-1/simple-monitor-in-cpp-koushik-philips/blob/b0227bf7f5112bd407d0467503cf773bd7d78c1a/resource_eng.lang) and [config file](https://github.com/code-craft-us-1/simple-monitor-in-cpp-koushik-philips/blob/b0227bf7f5112bd407d0467503cf773bd7d78c1a/localization.cfg) for selection.

## Off-the-shelf range evaluation

[Initialize the levels](https://github.com/code-craft-us-1/simple-monitor-in-cpp-koushik-philips/blob/b0227bf7f5112bd407d0467503cf773bd7d78c1a/vitalBaseline.cpp#L9) into a vector and [look for the lower bound](https://github.com/code-craft-us-1/simple-monitor-in-cpp-koushik-philips/blob/b0227bf7f5112bd407d0467503cf773bd7d78c1a/vital.cpp#L24) in it

## Complex, or not

```cpp
bool isPulseRateNotNormal(double pulseRate) {
    bool val = false;
    std::string str = "";
    if (!isVitalInRange(60, 100, pulseRate)) {
        str = "pulse_critical";
        val = true;
    }
    else if (isVitalInRange(100 - (100.0 * 0.015), 100, pulseRate)) {
        str = "warning_higherpulse";
        val = true;
    }
    else if (isVitalInRange(60, 60 + (60 * 0.015) , pulseRate)) {
        str = "warning_lowerpulse";
        val = true;
    }
    if (!str.empty()) {
       transMessage = getTranslation(str);
    }
    return val;
}
```

>Risk is that extra functionality (e.g., different pulse rate for children) would end up complicating this function further, making it harder to prove with tests. Harder to modify further as well.

## Duplication in tests

```cpp
TEST(Monitor, TempHigherWarningGerman) {
    CheckVitals vitals;
    vitals.SetLanguage(CheckVitals::Language::German);
    ASSERT_FALSE(vitals.vitalsOk(101, 70, 100));
    if (translations.find("warning_hyperthermia") != translations.end()) {
```

```cpp
TEST(Monitor, TempLowerWarningGerman) {
    CheckVitals vitals;
    vitals.SetLanguage(CheckVitals::Language::German);
    ASSERT_FALSE(vitals.vitalsOk(96, 70, 100));
    if (translations.find("warning_hypothermia") != translations.end()) {
```

>Duplication in tests? Ask yourself: What's the smallest test code that will prove the code? Can I test one aspect at a time? Will the code need to be re-organized to make that easier?
