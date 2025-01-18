# CSS Specificity Bug: !important and Inheritance

This repository demonstrates an uncommon CSS bug related to the `!important` declaration and specificity.  The bug showcases a scenario where a more specific selector fails to override a style declaration with the `!important` flag. This can lead to unexpected styling and make debugging more challenging.

**Bug Description:**
The `!important` flag in CSS has a higher precedence than the usual specificity rules. This means that a selector with `!important` will override even a more specific selector without the `!important` flag.

**How to Reproduce:**
1. Open `bug.css`.
2. Observe the styling on the `.child` element.
3. Note that the `color: green` from the `.parent .child` selector is overridden by `color: red !important` in the `.child` selector.

**Solution:**
Review `bugSolution.css` for an explanation and proper resolution.  Avoid using `!important` whenever possible to improve maintainability and predictability of your CSS styles.