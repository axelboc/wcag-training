# Accessibility issues

## Perceivable

### Text Alternatives

- Meaningful images displayed with `img` tags without text alternatives
- Meaningful image displayed with CSS without text alternative
- Decorative image not hidden from assistive technologies (background pattern)

### Adaptable

- No semantic elements to convey page structure, identify headings, etc.
- Text styled with bold/italic for emphasis without appropriate markup
- Paragraphs styled to look like headings
- List + list items for navigation slows down screen reader users (advisory)
- No visual difference between second and third-level headings (arguable)
- Wrong paragraph semantic around "Read the full article" links (arguable)

### Distinguishable

- No visual change when focusing navigation links and "Rate this article" button
- No visual change when hovering navigation links and "Read the full article" links (advisory)
- Colour alone used to identify inline links
- Colour change alone when hovering "Rate this article" button state (advisory)
- Insufficient contrast for page title (3:1)
- Insufficient contrast for navigation links and footer text (4.5:1)
- Insufficient contrast for inline links on hover (3:1)
- Page scaled incorrectly on mobile due to missing `viewport` tag
- Mininum width on body preventing reflow down to 320px (horizontal scroll)
- Navigation links cropped when resizing window down to 320px
- Navigation links cropped when zooming to 200% or setting `font-size: 200%` on small viewports

## Operable

### Keyboard accessible

- Button not focusable with keyboard because not a native `button`
- "Sports" navigation link not focusable with keyboard because of `tabindex="0"`

### Enough Time

- Moving text (`marquee` element) cannot be paused/stopped/hidden

### Navigable

- No landmark regions (because no structural markup)
- Page title is meaningless and doesn't match what is seemingly the title of the site (main heading on homepage)
- Wrong focus order for "Rate this article" button (assuming focusability is fixed)
- Purpose of "Read the full article" links is not clear from link text alone, label or context, and there are no alternative ways to access the article pages
- "Web Accessibility" link opens in a new tab but this is not conveyed to users (sighted or not)
- Limited ways to navigate to other pages (no sitemap, no search) - please disregard as example site is too contrived
- No focus outline on navigation links

### Input Modalities

- "Rate this article" button triggered on `mousedown` (prevents pointer cancellation)

## Understandable

### Readable

- Missing `lang` attribute on `html` element
- Abbreviation without access to expanded form ("ESRF")

## Robust

- Invalid `titel` attribute on "Web Accessibility" link
