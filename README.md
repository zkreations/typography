![typography](https://raw.githubusercontent.com/zkreations/typography/main/static/logo.png)

![J](https://img.shields.io/jsdelivr/npm/hm/@zkreations/typography?color=68D391) ![V](https://img.shields.io/npm/v/@zkreations/typography) ![L](https://img.shields.io/npm/l/@zkreations/typography)

**Typography** is a project designed to style basic text elements in HTML. It is especially useful in cases where you have no control over the generated HTML and cannot add classes directly.

## Features

- **Easy to use**: just add the `typography` class to the container you want to style.
- **Lightweight**: only **1KB** compressed with [Brotli](https://www.multiutil.com/text-to-brotli-compress/).
- **Responsive**: adapts without using media queries.
- **Modern**: leverages well-supported, cutting-edge CSS features.
- **Overridable**: low style specificity (**10**) for easy customization.
- **Decoupled**: HTML-based, without dependencies on specific structures.

## Installation

### NPM

```bash
npm install @zkreations/typography
```

### CDN

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@zkreations/typography@1/main.min.css">
```

## Usage

Add the `typography` class to the container that holds the elements you want to style:

```html
<div class="typography">
  <h1>Heading</h1>
  <p>This is a paragraph...</p>
</div>
```

## Customization

You can customize Typography's styles using CSS variables. Below are the available variables:

| Variable | Description | Default Value |
| -------- | ----------- | -------------- |
| `--typo-border-color` | Border color for elements | `#d4d4d4` |
| `--typo-caption-size` | Font size for captions | `0.875rem` |
| `--typo-caption-spacing` | Spacing between caption and element | `0.75rem` |
| `--typo-code-background` | Background for code | `#f5f5f5` |
| `--typo-code-padding` | Inner spacing for code | `1rem` |
| `--typo-column-min` | Minimum column width | `200px` |
| `--typo-gallery-caption-background` | Gallery caption background | `linear-gradient(#0000, #0006)` |
| `--typo-gallery-caption-color` | Gallery caption color | `white` |
| `--typo-gallery-caption-padding` | Gallery caption inner spacing | `0.75rem` |
| `--typo-gallery-min` | Minimum gallery width | `200px` |
| `--typo-gallery-spacing` | Spacing between gallery items | `2px` |
| `--typo-heading-spacing` | Spacing between headings | `1rem` |
| `--typo-initial-letter` | Initial letter size | `3` |
| `--typo-spacing` | Spacing between paragraphs | `1.5rem` |
| `--typo-spoiler-collapse-text` | Collapse text | `'Collapse'` |
| `--typo-spoiler-expand-text` | Expand text | `'Expand'` |
| `--typo-spoiler-padding` | Spoiler inner spacing | `1rem` |
| `--typo-table-cell-padding` | Table cell padding | `.5rem` |

> [!NOTE]
> You can override the value of CSS variables using any CSS selector, though it is recommended to use `:root`.

## Components

In addition to text styles, Typography includes some optional components you can use to add new features to your project:

| Class | Description |
| ----------- | ----------- |
| `.typo-align-left` | Aligns an element to the left with float. |
| `.typo-align-right` | Aligns an element to the right with float. |
| `.typo-align-center` | Centers an element. |
| `.typo-align-full` | Expands an element to 100% width. |
| `.typo-columns` | Distributes child elements into columns. |
| `.typo-gallery` | Distributes images into a gallery. |
| `.typo-drop-cap` | Applies a drop cap style to a paragraph. |
| `.typo-spoiler` | Creates an expandable/collapsible spoiler. |
| `.typo-table` | Prevents tables from overflowing. |
| `.typo-table-fixed` | Ensures a fixed table column layout. |

## Typography

### Paragraphs

```html
<p>This is a paragraph...</p>
<p class="typo-drop-cap">This is a paragraph with a drop cap...</p>
```

### Headings

```html
<h1>h1 Heading</h1>
<h2>h2 Heading</h2>
<h3>h3 Heading</h3>
<h4>h4 Heading</h4>
<h5>h5 Heading</h5>
<h6>h6 Heading</h6>
```

### Emphasis

```html
<strong>This is bold text</strong>
<em>This is italic text</em>
<u>This line of text will render as underlined.</u>
<a href="https://www.zkreations.com/">This is a link</a>
```

### Blockquote

```html
<blockquote>This is a blockquote.</blockquote>
```

### Ordered List

```html
<ol>
  <li>This is an ordered list</li>
  <li>All items are numbered sequentially</li>
</ol>
```

### Unordered List

```html
<ul>
  <li>This is an unordered list</li>
  <li>It is easy to read and understand</li>
</ul>
```

### Code

```html
<code>This is inline code</code>
<pre><code>This is a code block</code></pre>
```

### Table

```html
<figure class="typo-table">
  <table>
    <thead>
      <tr>
        <th>Heading 1</th>
        <th>Heading 2</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Row 1, Cell 1</td>
        <td>Row 1, Cell 2</td>
      </tr>
    </tbody>
  </table>
</figure>
```

### Spoiler

```html
<details class="typo-spoiler">
  <summary>Show and hide</summary>
  <p>This is a spoiler content</p>
</details>
```

### Accordion

```html
<details class="typo-spoiler" name='spoiler1'>
  <summary>First content</summary>
  <p>This is a first content</p>
</details>
<details class="typo-spoiler" name='spoiler1'>
  <summary>Second content</summary>
  <p>This is a second content</p>
</details>
```

> [!NOTE]
> You can use the `name` attribute to group spoilers and make them behave like an accordion. Only one of the spoilers with the same name will be open at a time.

### Columns

```html
<div class="typo-columns">
  <p>This is a paragraph in a column.</p>
  <p>All items are distributed in columns.</p>
</div>
```

### Separator

```html
<hr />
```

### Gallery

```html
<div class="typo-gallery">
  <img src="example.png" width="300" height="200" />
  <img src="example.png" width="300" height="200" />
  <img src="example.png" width="300" height="200" />
  <img src="example.png" width="300" height="200" />
</div>
```

### Gallery with Caption

```html
<div class="typo-gallery">
  <figure>
    <img src="example.png" width="300" height="200" />
    <figcaption>Figure 1</figcaption>
  </figure>
  <figure>
    <img src="example.png" width="300" height="200" />
    <figcaption>Figure 2</figcaption>
  </figure>
</div>
```

## Overriding Styles

Typography's styles have a low specificity (`10`), making them easy to override or modify with new styles. A good way to do this is by using a class selector followed by the element you want to style:

```css
/* Total specificity: 11 */
.typography blockquote {
  color: #f00;
  font-style: italic;
}
```

This method also helps create more complex styles and unique designs tailored to your needs.

## Supporting

If you want to help me keep this and more related projects always up to date, you can [buy me a coffee](https://ko-fi.com/zkreations) ☕. I will be very grateful 👏.

## License

**typography.css** is licensed under the MIT License.
