# Temporal API Cheat Sheet

A quick reference for the Temporal API, part of the ECMAScript proposal for modern date and time handling.

---

## 🕒 Core Concepts

- **Plain**: Date/time without time zone (e.g., `PlainDate`, `PlainTime`).
- **Zoned**: Date/time with a time zone (e.g., `ZonedDateTime`).
- **Duration**: A length of time, independent of specific start/end.
- **Instant**: A fixed point in time (similar to `Date.now()` but more precise).

---

## 🛠️ Creating Temporal Objects

```javascript
const now = Temporal.Now.instant();                // Current instant
const today = Temporal.Now.plainDateISO();         // Current date (ISO calendar)
const time = Temporal.Now.plainTimeISO();          // Current time
const date = Temporal.PlainDate.from('2025-05-26');
const time = Temporal.PlainTime.from('12:30:00');
const dateTime = Temporal.PlainDateTime.from('2025-05-26T12:30:00');
const zoned = Temporal.ZonedDateTime.from('2025-05-26T12:30:00+01:00[Europe/London]');
const duration = Temporal.Duration.from({ hours: 2, minutes: 30 });
```

### 🔄 Formatting
```javascript
date.toString();           // '2025-05-26'
time.toString();           // '12:30:00'
dateTime.toPlainDate();    // PlainDate object
```


### ⏱️ Duration
- Represents a length of time.
- Not tied to specific start or end points.

```javascript
const duration = Temporal.Duration.from({ days: 3, hours: 4 });
duration.total({ unit: 'hours' });   // Total hours
```

### 🌍 Working with Time Zones
```javascript
const zoned = Temporal.ZonedDateTime.now('America/New_York');
zoned.toPlainDateTime();    // Converts to PlainDateTime
zoned.withTimeZone('UTC');  // Change time zone
```

### 📅 Comparing Dates

```javascript
Temporal.PlainDate.compare(date1, date2);  // -1, 0, or 1
date.equals(anotherDate);                  // true or false
```

### 📏 Difference Between Dates
```javascript
const diff = date1.until(date2);   // Temporal.Duration object
const diffDuration = date1.since(date2);
```

### 🧹 Rounding
```javascript
const rounded = Temporal.Instant.from('2025-05-26T12:30:45Z')
.round({ smallestUnit: 'minute' });  // '2025-05-26T12:31:00Z'
```

## ❓ Why use Temporal?

✅ Immutable objects  
✅ Safer than `Date`  
✅ Built-in support for time zones  
✅ Precise arithmetic with durations  
✅ Clear and consistent API  

---

## 📝 Useful Patterns

- Use `Temporal.Now.*` for current time data.
- Prefer `ZonedDateTime` for operations involving time zones.
- Use `Duration` for time spans (e.g., delays, intervals).

---

## 📚 Resources

- [TC39 Temporal Proposal](https://tc39.es/proposal-temporal/)
- [MDN Temporal Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Temporal)
- [Polyfill](https://github.com/tc39/proposal-temporal#polyfill)
"""

[Voltar para HOME](https://github.com/pvstelles/cheat-sheet/blob/main/README.md)

  
