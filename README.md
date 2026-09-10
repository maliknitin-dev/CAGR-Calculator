# CAGR Calculator

A simple, self-contained **Compound Annual Growth Rate (CAGR)** calculator that runs in any web browser.

## What is CAGR?

CAGR is the steady yearly growth rate that would take you from a starting value
to an ending value over a number of years, as if the growth happened evenly
(compounded) every year.

```
CAGR = (Final ÷ Initial) ^ (1 ÷ Years) − 1
```

## How to run it

No installation, no build step, no internet needed.

1. Open the `index.html` file.
2. On Windows you can just **double-click** `index.html`, or right-click → *Open with* → your browser.
3. Enter your numbers and click **Calculate CAGR** (or press **Enter**).

## How to use it

| Field | What to type | Example |
|-------|--------------|---------|
| **Initial value** | Your starting amount (decimals allowed) | `1000.50` |
| **Final value** | Your ending amount (decimals allowed) | `1650.75` |
| **Number of years** | The time between the two values (decimals allowed) | `5` |

The result shows the CAGR as a percentage, plus a line telling you what
percentage the final value is of the initial value.

> **Why three inputs?** CAGR is an *annual* rate, so it needs to know how many
> years passed between the two values. With only two values you could calculate
> *total* growth, but not the *annual* growth rate.

## Example results

| Initial | Final | Years | CAGR |
|---------|-------|-------|------|
| 100.00 | 200.00 | 10 | 7.18% |
| 1000.50 | 1650.75 | 5 | 10.54% |
| 500.00 | 250.00 | 3 | −20.63% (a decline) |
| 100.00 | 100.00 | 5 | 0.00% (no change) |

## Files

| File | Description |
|------|-------------|
| `index.html` | The entire app: HTML (structure), CSS (looks), and JavaScript (logic). Every JavaScript function is commented to explain what it does. |

## Functions in `index.html`

| Function | Purpose |
|----------|---------|
| `parseNumber` | Converts the text typed in a box into a real number (or `NaN` if blank/invalid). |
| `validateInputs` | Checks the numbers for problems and returns a friendly error message. |
| `calculateCAGR` | Runs the CAGR formula and returns the result as a decimal. |
| `formatPercent` | Turns a decimal like `0.0718` into the text `"7.18%"`. |
| `showError` | Shows a red error message and hides the result. |
| `clearError` | Hides the red error message. |
| `showResult` | Shows the green result box with the answer. |
| `handleCalculate` | The "traffic controller" that runs when you click Calculate or press Enter. |

## Input rules

- Initial value must be **greater than zero**.
- Final value must **not be negative**.
- Number of years must be **greater than zero** (decimals like `2.5` are allowed).
