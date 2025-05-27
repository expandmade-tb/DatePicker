# Datepicker Component

A lightweight, customizable, and accessible datepicker component for easy integration into web applications. This JavaScript-based datepicker supports multiple formats, languages, and navigation features

### Why Another Datepicker?

I created this datepicker because I was looking for a **simple, lightweight solution** in **plain JavaScript** that:

- **Has a small codebase**: Avoids the overhead of large libraries or frameworks.
- **Supports multiple languages**: Makes it easy to localize for different users (currently supports English, German, and Spanish).
- **Offers a few flexible date formats**: Without overcomplicating the configuration (formats like `yyyy-mm-dd`, `dd.mm.yyyy`, and `mm/dd/yyyy`).

Many existing datepickers are either too complex or rely on heavy dependencies like jQuery, which can bloat your project. This one is **minimal**, **easy to integrate**, and **fast**, making it a perfect choice for those who want just the essential functionality without extra bloat.

## Features
- **Customizable Date Formats**: Supports multiple date formats, including `dd.mm.yyyy`, `mm/dd/yyyy`, `yyyy-mm-dd`, and more.
- **Language Support**: Currently supports `en` (English), `de` (German), and `es` (Spanish) for localization.
- **Navigation Controls**: Navigate through months with next/previous buttons.
- **Mobile-Friendly**: Optimized for mobile and touch support.
- **Accessibility**: Designed with accessibility in mind, including keyboard navigation and focus management.
- **Flexible Positioning**: Automatically positions the calendar based on available space.

## Installation

### Using npm
```bash
npm install your-datepicker-library
````

### Using CDN

```html
<link rel="stylesheet" href="https://cdn.example.com/datepicker.min.css">
<script src="https://cdn.example.com/datepicker.min.js"></script>
```

## Usage

### HTML + JavaScript

```html
<link rel="stylesheet" href="datepicker.min.css">
<input type="text" id="datepicker">
<script src="datepicker.min.js"></script>
<script>
  const datepicker = new Datepicker('#datepicker', 'yyyy-mm-dd', 'en');
</script>
```

### JavaScript Code

#### `Datepicker` Class

* **Constructor Parameters**:

  * `selector` (string): The CSS selector for the input element.
  * `format` (string): The date format (`'dd.mm.yyyy'`, `'mm/dd/yyyy'`, `'yyyy-mm-dd'`, `'Y-m-d'`).
  * `lang` (string): Language for localization (`'en'`, `'de'`, `'es'`).

```javascript
const datepicker = new Datepicker('#datepicker', 'yyyy-mm-dd', 'en');
```

#### Features:

* **Format Validation**: Valid formats are `'dd.mm.yyyy'`, `'dd/mm/yyyy'`, `'mm/dd/yyyy'`, `'yyyy-mm-dd'`, `'Y-m-d'`.
* **Language Localization**: Supports `'en'`, `'de'`, and `'es'` for month names, weekdays, and "Today" button text.
* **Positioning**: The calendar automatically positions itself based on available space relative to the input field.

#### Methods:

* `showCalendar()`: Displays the calendar, positioning it relative to the input field.
* `hideCalendar()`: Hides the calendar when clicking outside or pressing "Escape".
* `renderCalendar()`: Renders the calendar UI, including days, weekdays, and navigation buttons.
* `parseDate(str)`: Parses the date string based on the selected format.
* `formatDate(date)`: Formats the date in the selected format.

## Configuration Options

| Option   | Type   | Description                                                                                                     |
| -------- | ------ | --------------------------------------------------------------------------------------------------------------- |
| `format` | String | The date format. Available formats: `dd.mm.yyyy`, `mm/dd/yyyy`, `yyyy-mm-dd`, `Y-m-d`. Default is `yyyy-mm-dd`. |
| `lang`   | String | The language for localization. Options: `en`, `de`, `es`. Default is `en`.                                      |

## Example

Here's a simple example of how to initialize the datepicker on an input field:

```html
<input type="text" id="datepicker" placeholder="Select a date">
<script>
  const datepicker = new Datepicker('#datepicker', 'yyyy-mm-dd', 'en');
</script>
```

### Navigation

* **Prev & Next Buttons**: Use the left (`←`) and right (`→`) arrows to navigate through months.
* **Today Button**: Click the "Today" button to set the input to the current date.
