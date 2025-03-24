Who need this fix edit the wled.cpp and move the:
``` 
 handlePresets();
  yield();
```

before:

```
if (!realtimeMode || realtimeOverride || (realtimeMode && useMainSegmentOnly))
```
