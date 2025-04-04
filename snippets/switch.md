# 🔁 SWITCH / CASE

Use `SWITCH` to evaluate values against different `CASE`s.

## ✅ Example

```snippet
SWITCH color {
  CASE "Red" {
    TRACE("Stop")
  }
  CASE "Green" {
    TRACE("Go")
  }
  DEFAULT {
    TRACE("Unknown")
  }
}
```
