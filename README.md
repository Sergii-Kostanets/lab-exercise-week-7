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


**The Console message when I mistyped the id, and what `null` means:**


**When I use `const` and when I use `let`:**


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

