# CodeWars JavaScript Solutions

## Deodorant Evaporator

This program tests the life of an evaporator containing a gas.

We know the content of the evaporator (content in ml), the percentage of foam or gas lost every day (evap_per_day) and the threshold (threshold) in percentage beyond which the evaporator is no longer useful. All numbers are strictly positive.

The program reports the nth day (as an integer) on which the evaporator will be out of use.

Example:

```
evaporator(10, 10, 5) -> 29
```

**Note:**

Content is in fact not necessary in the body of the function "evaporator", you can use it or not use it, as you wish. Some people might prefer to reason with content, some other with percentages only. It's up to you but you must keep it as a parameter because the tests have it as an argument.

### Solution

```javascript
const evaporator = (content, evapPerDay, threshold) => {
  let outOfUseDays = 0,
    percentage = 100;
  while (percentage > threshold) {
    percentage = percentage - percentage * (evapPerDay / 100);
    outOfUseDays += 1;
  }
  return outOfUseDays;
};

let days,
  percent = 100;
```

[See on CodeWars.com](https://www.codewars.com/kata/5506b230a11c0aeab3000c1f/javascript)