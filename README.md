
# SpendWise Dashboard Shell

## Project Description

SpendWise is a modern and responsive personal finance dashboard designed to help users visualize their income, expenses, savings, and spending categories.

This project focuses on building the visual foundation of the SpendWise capstone project using HTML and modern CSS techniques. No JavaScript functionality is required at this stage.

## Features

- Responsive dashboard layout
- Sidebar navigation menu
- Dashboard header with user profile
- Financial summary cards
- Six expense category cards
- CSS Grid for the overall page structure
- Flexbox for internal component layouts
- CSS custom properties for theming
- Responsive design for smaller screens
- Hover and keyboard-focus micro-interactions
- Dark theme using the user's system preference

## Expense Categories

The dashboard includes six realistic financial categories:

1. Food
2. Transport
3. Rent
4. Entertainment
5. Savings
6. Utilities

Each category displays static financial information, including an expense amount, percentage, description, and progress indicator.

## Layout Techniques

### CSS Grid

CSS Grid is used for the overall dashboard structure.

The layout contains:

- A sidebar
- A main content area
- A responsive category card grid

Example:

```css
.dashboard {
    display: grid;
    grid-template-columns: 240px 1fr;
}
````

### Flexbox

Flexbox is used to arrange content inside:

* Sidebar navigation
* Header
* User profile
* Summary cards
* Dashboard cards
* Card headers

The project does not use absolute positioning for the page layout.

## CSS Custom Properties

The application theme is defined using CSS custom properties inside the `:root` selector.

The main theme variables include:

```css
:root {
    --brand-color: #2563eb;
    --accent-color: #16a34a;
    --surface-color: #ffffff;
    --background-color: #f5f7fb;
    --primary-text: #1f2937;
    --secondary-text: #64748b;
}
```

These variables are reused throughout the stylesheet to maintain a consistent design.

## Responsive Design

The dashboard is responsive and adapts to smaller screens.

Below 768px:

* The dashboard changes to a single-column layout.
* The sidebar navigation becomes horizontal.
* Summary cards stack vertically.
* Expense category cards stack into one column.
* The header adjusts to fit smaller screens.

The responsive layout can be tested using the browser's DevTools Device Toolbar.

### Testing Responsive Design

In Google Chrome:

1. Open `index.html`.
2. Right-click the page.
3. Select **Inspect**.
4. Click the **Device Toolbar** icon.
5. Select a mobile device such as an iPhone or Pixel.
6. Resize the screen and verify that the dashboard changes to a single-column layout.

## Card Micro-interactions

Dashboard cards include subtle hover and keyboard-focus effects.

The animations use:

* `transform`
* `box-shadow`
* `transition`

The animation duration is 200ms, which is below the required 250ms limit.

Example:

```css
.category-card {
    transition:
        transform 200ms ease,
        box-shadow 200ms ease;
}

.category-card:hover,
.category-card:focus {
    transform: translateY(-4px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
}
```

The cards use `tabindex="0"` so they can also receive keyboard focus.

## Dark Theme

As a stretch goal, SpendWise supports a dark theme using the user's operating-system color preference.

The dark theme overrides the CSS custom properties inside:

```css
@media (prefers-color-scheme: dark)
```

This allows the same dashboard to automatically adapt to light or dark system preferences without changing the HTML structure.

## Project Structure

```text
spendwise/
│
├── index.html
├── style.css
└── README.md
```

## Technologies Used

* HTML5
* CSS3
* CSS Grid
* Flexbox
* CSS Custom Properties
* CSS Media Queries
* Google Fonts

## Current Scope

This version of SpendWise is a visual dashboard shell only.

There is currently no:

* JavaScript functionality
* Database
* User authentication
* Dynamic expense tracking
* Data persistence

Functionality can be added in later stages of the capstone project.

## Author

SpendWise Dashboard Shell

```
```
