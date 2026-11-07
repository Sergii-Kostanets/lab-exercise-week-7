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
Changes to Open successfully

**Puzzle 2:**
- Water
- Coffee
- Cocoa

**Puzzle 3:**
Was: Price: 5 euro

**Puzzle 4:**
Seats left: 13

**Puzzle 5:**
Weather report to follow. (Uncaught TypeError: Cannot set properties of null (setting 'textContent') - in the console)

**Puzzle 6:**
Score: not played yet (Uncaught TypeError: Assignment to constant variable - in the console)

**Puzzle 7:**
Pass 3, and then i is 3

**Puzzle 8:**
Pass 3

**For each wrong prediction: what the page showed, and why:**
- Puzzle 7
- Pass 3, and then i is 4
- because the loop increments `i` to 4 before it stops.

## Tickets: what was wrong, and what I changed

**Ticket 1:**
Remove extra s in the ID

**Ticket 2:**
Move script to the bottom of the body

**Ticket 3:**
Replace small b to capital B in getElementById

**Ticket 4:**
replace querySelector from li to .weekend

## Validator results
No errors

# Exercise 2 notes: Changing the content

**Name:** Sergii Kostanets

## market-stall.html

**What the same string looked like through `textContent`, and through `innerHTML`:**

The string `Today: <i>half price</i> on all jars.` appears literally, including
the `<i>` tags, when assigned through `textContent`. Through `innerHTML`, the
browser interprets the tags, so “half price” appears in italics.

**When `innerHTML` is the right tool, and when it is not:**

Use `innerHTML` when intentionally inserting trusted HTML markup, as with the
formatted stall summary. Use `textContent` for plain text, especially for
untrusted text, because it displays text without interpreting it as HTML.

**The difference between `link.href` and `link.getAttribute('href')`:**

`menuLink.href` returns the link URL as an absolute, resolved URL.
`menuLink.getAttribute('href')` returns the value written in the `href`
attribute. In this page, the script sets that attribute to the absolute URL
`https://example.org/stall-menu`, so both return that URL.

## picnic-list.html

**What the page showed before I added `append`, and why:**

The page showed the “Picnic list” heading and the draft label,
“Draft: still checking the weather.” The list items had been created and
filled with text, but they were not attached to the page, so they did not
appear.

**The three steps for a new element:**

1. Create the element with `document.createElement('li')`.
2. Fill it with text using `listItem.textContent = food`.
3. Attach it to the list with `picnicItems.append(listItem)`.

## Puzzles: my predictions (before opening any page)

**Puzzle 1:**
Welcome

**Puzzle 2:**
```Sale: <b>half price</b>```

**Puzzle 3:**
Sale: <b>half price</b>

**Puzzle 4:**
- Green
- Black

**Puzzle 5:**
- More information
- Goes to https://example.org/new

**Puzzle 6:**
- Bread

**Puzzle 7:**
- Red
- Green
- Blue

**Puzzle 8:**
- One
- Three

**For each wrong prediction: what the page showed, and why:**
- All correct


## Tickets: what was wrong, and what I changed

**Ticket 1:**
Replace textContent to innerHTML

**Ticket 2:**
Add dayList.appendChild(dayItem); inside the for loop

**Ticket 3:**
Add () to oldNotice.remove

**Ticket 4:**
Move const nameItem = document.createElement('li'); into the for loop

## Validator results
No errors


# Exercise 3 notes: Events

**Name:** Sergii Kostanets

## cafe-board.html

**What the page did with `showSpecial()` with brackets, and why:**

The special appeared as soon as the script ran, before I clicked the button,
because `showSpecial()` called the function immediately.

**What happened when the script was in the head, and the Console message:**

Nothing happened when I clicked the button because the script ran before the
browser had read the button. `getElementById` returned `null`, so the Console
showed: `Uncaught TypeError: Cannot read properties of null (reading
'addEventListener')`.

## lap-log.html

**What the total showed before I used `Number`, and why:**

The total treated the input as text instead of a number. For example, entering
`20` and then `15` would show `Total lengths: 02015`, because `+` concatenated the
input strings instead of adding their numeric values.

**Why `totalLengths` is declared with `let`, and outside the function:**

It is declared outside `addLengths()` so its value is preserved between
button clicks. It uses `let` because the total is reassigned whenever lengths
are added or the log is reset.

**What `Number.isNaN` is for:**

`Number.isNaN(lengthsSwum)` checks whether the input converted to `NaN`
(“Not-a-Number”), so the page can reject text that is not a valid number.
The separate empty-string check is needed because `Number('')` is `0`.

## name-badge.html

**How the `input` event differs from the `click` event:**

The `input` event fires whenever the text in the field changes, so the badge
preview updates as I type. A `click` event fires when an element is clicked,
so it would not respond to each change in the text unless I clicked something.

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


# Exercise 4 notes: Styles

**Name:** Sergii Kostanets

## platform-board.html

**The style attribute I saw in the Elements panel:**


**What reloading did to it, and why:**


## canteen-menu.html

**The class attribute after each click:**


**What happened with the dot in the class name:**


**When I would use the `style` property, and when `classList`:**


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
