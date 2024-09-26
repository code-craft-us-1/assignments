# Passing tests recap

What if the complexity increases in the weather forecasting rules?

```cpp
if (sensor.TemperatureInC() > 25) {
    if (precipitation >= 20 && precipitation < 60) {
        report = "Partly cloudy";
    } else if (precipitation >= 60) {
        report = "Expect rains today";
        if (sensor.WindSpeedKMPH() > 50)
            report = "Alert, Stormy with heavy rain";
    }
}
return report;
```

---

Let the assert express the customer need. What does this express?

```cpp
assert(report.find("rain") != string::npos);
```
