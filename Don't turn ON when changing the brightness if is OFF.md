Who need this fix edit the json.cpp -> deserializeState:

```
  bool onBefore = bri;
  bool on = root["on"] | (bri > 0);

  if (on) {
    getVal(root["bri"], &bri);
  } else {
    getVal(root["bri"], &briLast);
  }

  if (!on != !bri) toggleOnOff();
```

And use {"bri":xyz} instated of A=
