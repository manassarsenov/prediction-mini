# Prediction Mini

Open `index.html` in a file manager on Windows, macOS, or Linux. This is the entry point; paths with spaces are fine. No external dependencies, network connection, server, Python, Node, or npm are needed.

Enter a whole number from 0 to 100 in Quantity and select Calculate. The user supplies the input; the application does not load a dataset. The result is in demo units, not USD.

`app.js` contains the fixed educational calculation `10 + 20 × Quantity`. It is not a real or trained model, and there is no trained artifact. `samples/control_examples.json` records the control examples:

- Quantity 2 → 50 demo units
- Quantity 0 → 10 demo units
- Quantity 5 → 110 demo units

Empty input, −1, 2.5, 101, and text should produce a clear error. Open `checks.html` in the file manager to execute the calculation checks and see PASS or FAIL for each case. A label change should not change the results.

## Threshold demo for M4C2

Open `threshold-demo.html` by double-clicking it. This standalone page also works if copied into your existing M4C1 project folder. It needs no installation or network connection.

The editable value is a synthetic example, not a result from a trained model. The fixed threshold is 0.50: a value below it produces **No alert**; a value equal to or above it produces **Alert**. Change only the visible label `Score` to `Churn probability (0–1)` for the lesson; keep the rule and calculation unchanged.

Select **Check** after each input:

- 0.42 → `p=0.42 → No alert`
- 0.50 → `p=0.50 → Alert` (equality included)
- 0.72 → `p=0.72 → Alert`
- 0 and 1 are accepted; an empty value, a negative number, or a number above 1 displays an error and no result.

The original `index.html` and `checks.html` remain available for the earlier calculation exercise.
