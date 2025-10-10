A simple circuit design for keeping track of the passage of time in ticks.

Connect the output of a decider combinator back to its input, and configure:

![Screenshot_20251009_164824](../attachments/Screenshot_20251009_164824.png)
> Output `Clock = Previous Clock + 1` if `Previous Clock` < 60 ticks

The condition `< 60` has the Clock loop back around after 60 ticks (one second), so configure that to whatever interval you would prefer.

## Variations
- Setting the condition to always be true would result in the counter incrementing indefinitely (or at least until the combinator runs out of power). This is usually undesirable
- Replacing the condition with another condition can let you keep track of the elapsed time since that condition was false.