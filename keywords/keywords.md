# 📘 Interactive Keyword Reference

Welcome to the **NICE CXone Studio Keyword Guide**. These keywords are used in Snippet code blocks to control flow, logic, loops, and more.

## 🔧 Code Block Test

Here's a sample keyword usage:

```snippet
ASSIGN score = 100
IF score > 90 {
  TRACE("Great job!")
}
```
---

## 📚 Table of Contents

- [Variable & Function Keywords](#variable--function-keywords)
- [Conditional Logic Keywords](#conditional-logic-keywords)
- [Looping Keywords](#looping-keywords)
- [Utility & Debugging Keywords](#utility--debugging-keywords)

---

## 🧠 Keyword Syntax Notes

- Keywords **must be the first word** on a line.
- They are **not case-sensitive**.
- Code blocks are enclosed in `{ }`.
- Use `//` for comments.

---

## 📦 Variable & Function Keywords

<details>
<summary><strong>ASSIGN</strong> – Declare and assign a variable</summary>

```snippet
ASSIGN score = 100
```

Assigns a value to a variable. Variables can be updated later in the script.

</details>

<details>
<summary><strong>DYNAMIC</strong> – Create a dynamic key-value object</summary>

```snippet
DYNAMIC customer
ASSIGN customer.name = "Troy"
```

Useful for building objects like JSON.

</details>

<details>
<summary><strong>FUNCTION / RETURN</strong> – Create reusable logic blocks</summary>

```snippet
FUNCTION Add(x, y) {
  RETURN x + y
}
```

Functions encapsulate logic and return values for reuse.

</details>

---

## 🔀 Conditional Logic Keywords

<details>
<summary><strong>IF / ELSE</strong> – Evaluate a condition</summary>

```snippet
IF score > 90 {
  TRACE("High score!")
} ELSE {
  TRACE("Keep trying!")
}
```

Use `ELSE` to catch the opposite condition.

</details>

<details>
<summary><strong>SWITCH / CASE / DEFAULT</strong> – Compare a variable to multiple cases</summary>

```snippet
SWITCH status {
  CASE "Open" {
    TRACE("Case is open")
  }
  CASE "Closed" {
    TRACE("Case is closed")
  }
  DEFAULT {
    TRACE("Unknown status")
  }
}
```

Use `DEFAULT` to catch unmatched cases.

</details>

<details>
<summary><strong>SELECT</strong> – Similar to SWITCH but based on Boolean conditions</summary>

```snippet
SELECT {
  CASE score > 90 {
    TRACE("A")
  }
  CASE score > 80 {
    TRACE("B")
  }
}
```

Runs the first case that evaluates to true.

</details>

---

## 🔁 Looping Keywords

<details>
<summary><strong>FOR</strong> – Classic counter-based loop</summary>

```snippet
FOR i = 1 TO 5 {
  TRACE("Iteration: " + i)
}
```

Runs the loop while `i` is between 1 and 5.

</details>

<details>
<summary><strong>FOREACH</strong> – Loop through each element in an array</summary>

```snippet
FOREACH item IN itemList {
  TRACE(item)
}
```

Iterates over all values in a collection.

</details>

<details>
<summary><strong>REPEAT</strong> – Run block a fixed number of times</summary>

```snippet
REPEAT 3 TIMES {
  TRACE("Repeat!")
}
```

Good for simple, fixed repetition.

</details>

<details>
<summary><strong>BREAK</strong> – Exit a loop early</summary>

```snippet
FOR i = 1 TO 10 {
  IF i == 3 {
    BREAK
  }
  TRACE(i)
}
```

Breaks the loop when `i` is 3.

</details>

---

## 🛠 Utility & Debugging Keywords

<details>
<summary><strong>TRACE</strong> – Output to Trace panel (debugging)</summary>

```snippet
ASSIGN message = "Start"
TRACE("Message: " + message)
```

Use for debugging logic and variable flow.

</details>

<details>
<summary><strong>USES</strong> – Import a web service DLL</summary>

```snippet
USES "myProxy.dll"
```

Advanced use for calling external web services.

</details>

---

## ✅ Notes & Tips

- Use `TRACE` generously during development; remove or disable in production.
- Always include `DEFAULT` in a `SWITCH` for safety.
- Modularize using `FUNCTION` to simplify complex logic.
- Group related code using consistent indentation and comments.

---

🔗 Back to [Home](/README.md)
