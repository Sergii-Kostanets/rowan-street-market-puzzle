# Exercise 2 notes: Rowan Street Market

Name:

## PART 1: MY PREDICTIONS (written before opening the page)
1. Opening paragraph: dimgray (`main p` beats `p`).
2. "Please bring your own bags": crimson (`.note` beats `main p`).
3. "Tip: come before ten": seagreen and italic (`.tip` and `.note` have equal specificity; `.tip` is later).
4. "Today only": darkorange (`#deal` beats the class selectors).
5. "Cheese and butter": purple (`.stalls li` beats `.sale` because both have one class and `.stalls li` also has an element selector).
6. "Apples and pears": teal (the inline style wins).
7. Footer sentence: black, italic (`p` sets the color; italic is inherited from `footer`).
8. Footer link: dimgray, italic (the inherited color from `footer` would beat the browser's default link color).

## PART 2: WHAT CHROME SHOWS
8. The link is browser-default blue, not dim gray. The browser's default link color is applied to the link itself, so it beats the inherited color from `footer`. Inherited values are weaker than rules applied directly to an element, including the browser's built-in link styling. The link is still italic because it inherits `font-style: italic` from `footer`.

## PART 3: THE FIVE TICKETS
Ticket 1: `.stalls li` was winning because it has one class and one element selector, while `.sale` has only one class. I changed `.sale` to `.stalls .sale`, giving the sale rule two classes so it wins and makes "Cheese and butter" firebrick.
Ticket 2: `#deal` was winning because an id is more specific than the `.note` class, so "Today only" was dark orange. I changed the `#deal` rule to crimson and added `font-weight: bold`.
Ticket 3: The inline `style="color: teal"` won because inline styles take precedence over the stylesheet. I removed the inline style from "Apples and pears"; the sale rule now makes it firebrick.
Ticket 4: The `p` rule gave the footer paragraph black directly, and the browser's link styling gave the link blue directly; both beat the inherited dimgray from `footer`. I added `footer p, footer a { color: dimgray; }` so both elements receive dimgray directly.
Ticket 5: `.tip` won over `.note` because both selectors have one class and `.tip` appears later. I changed `.tip`'s color to crimson and left `font-style: italic` unchanged.
