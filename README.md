# Exercise 1 notes: Finding and changing

**Name:** Sergii Kostanets

## allotment.html

**What the file on disk says, and what the page in the browser says, after the script has run:**

On disk, before the script runs:

- Open on Saturdays from ten until noon.
- Water your plot before nine in the morning.
- Bring your own tools.
- Take rubbish home with you.
- The gate code is on the noticeboard.

In the browser, after the script runs:

- Open on Saturdays and Sundays from ten until noon.
- Water your plot before nine, or after six in the evening.
- Bring your own tools and a watering can.
- Take rubbish home with you.
- The gate code is on the noticeboard.

**Why `querySelector('ul li')` changed only one item:**

`document.querySelector('ul li')` returns only the first element that matches
the selector: the first `<li>` inside a `<ul>`. The variable `firstRule` stores
that single element, so changing its `textContent` changes only that item.
`firstRule` is a variable name, not a JavaScript method.

## plot-count.html

**The Console message when I changed `let` to `const`:**

`Uncaught TypeError: Assignment to constant variable.`

This happens because `freePlots` is declared with `const`, then the script
tries to assign it a new value with `freePlots = freePlots - 3`. A `const`
variable cannot be reassigned. The error stops the script at that line, so
the following line does not update the page and it still says
`Free plots: unknown`.

**The Console message when I mistyped the id, and what `null` means:**

`Uncaught TypeError: Cannot set properties of null (setting 'textContent')`

I mistyped the id as `'free-plot'` instead of `'free-plots'`. Since no element
has the id `'free-plot'`, `document.getElementById('free-plot')` returns
`null`. Here, `null` means that no matching element was found. The next line
tries to set `textContent` on that `null` value, causing the error and stopping
the script. The page therefore keeps showing `Free plots: unknown`.

**When I use `const` and when I use `let`:**

Use `const` for a variable whose value will not be reassigned. Use `let` when
the variable needs to be assigned a different value later, as with
`freePlots` when its count changes from 12 to 9.

## Puzzles: my predictions (before opening any page)

**Puzzle 1:**

**Puzzle 2:**

**Puzzle 3:**

**Puzzle 4:**

**Puzzle 5:**

**Puzzle 6:**

**Puzzle 7:**

**Puzzle 8:**

**For each wrong prediction: what the page showed, and why:**


## Tickets: what was wrong, and what I changed

**Ticket 1:**

**Ticket 2:**

**Ticket 3:**

**Ticket 4:**

## Validator results
