# Recap of reducing complexity

What do we call this functionality?

```cpp
for (int i = 0; i < 6; i++) {
    cout << "\r* " << flush;
    sleep_for(seconds(1));
    cout << "\r *" << flush;
    sleep_for(seconds(1));
}
```

```
GenerateWarning
DisplayCriticalIndicator
displayWarningPrompt
printWarningGraphics
sleep
```

Or combine it with `cout << message;`:

```
displayAlert
showMessage
PrintError
```

---

How about this one?

```cpp
if (value < min || value > max) {
    return false;
} else {
    return true;
}
```

```
isVitalNormal
CheckValueOutOfRange
checkVital
```

---

How about summarizing the result?

```cpp
return tempStatus && pulseRateStatus && spo2Status;
```

```
isPatientCritical
vitalsOk
checkVitalStatus
```

## Flexibility

Declarative style [using arrays and vectors](https://github.com/code-craft-us-1/simple-monitor-in-cpp-srivathsa-sarvothama/blob/2976f77127ecf902ee224a10fc535d2d0844abaa/monitor.cpp)

[Collect the results to summarize](https://github.com/code-craft-us-1/simple-monitor-in-cpp-HariPhilips/blob/f9ca21930bcab65982211dff75d00cd360820668/monitor.cpp)

Patient is not-ok when [any vital](https://github.com/code-craft-us-1/simple-monitor-in-cpp-ranjithjp/blob/548ce5a0928899c3cd494c367cf37a60d596bad0/monitor.cpp) is off range

## Tests

[Property based tests](https://github.com/code-craft-us-1/simple-monitor-in-cpp-Sriranganatha1979/blob/6166c35f28bab05080bf9a45b025983ea5caf1b2/test-monitor.cpp)

[Lower semantic distance](https://github.com/code-craft-us-1/simple-monitor-in-cpp-GauravKh01/pull/1/files) in range comparison gives 100% coverage without adding more tests!
