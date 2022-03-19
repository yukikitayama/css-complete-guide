# CSS - The Complete Guide 2022 (incl. Flexbox, Grid & Sass)

- [CSS - The Complete Guide 2022 (incl. Flexbox, Grid & Sass)](https://www.udemy.com/course/css-the-complete-guide-incl-flexbox-grid-sass/)

## Add CSS

- Add `inline` sytle by `<HTML_TAG style="PROPERTY: VALUE"></HTML_TAG>` in HTML elements
  - Not recommended because when style gets complex, hard to manage.
  - `"PROPERTY: VALUE"` is called declaration.
- Add `<style>` tag to `<head>` section with selector.
- Value: `inherit`, meaning 

## Selector

- `class`
  - In any HTML elements, add `class="CLASS_NAME"`
  - And CSS file define with dot like `.class_name { PROPERTY: VALUE; }`
  - Class name should use Cabab case e.g. `xxx-yyy` by using hyphens.
  - CSS is case-insensitive.
  - Class is very if you have a chance to use it again
- `Cascading style sheets specificity`
  - `inline` styles is the highest.
  - `ID` selector is the second highest.
  - `class`, `pseudo-class`, `attribute` selectors have high specificity
  - `tag`, `pesudo-element` selectors have low specificity.
- `Inheritance`
  - Child elements inherit the styles of the direct and indirect parents.
  - Inheritance always has the bottom specificity.

## Combinator

- `Decendent` would be the most frequent use. It doesn't matter whether it's direct child or indirect (nested) child. It will apply the rule to all the children.
  - Use `div p {}` style in CSS.

## Property Worth to Remember

- `color`
- `background-color`
- `display`
- `padding`
- `border`
- `margin`
- `width`
- `height`

## Default CSS

- `body` has a margin. To suppress it, `body { margin: 0; }`
- `h1` has top and bottom margin.

## Margin Collapsing

- If two margins overlapps, a bigger margin wins, so it won't have a too big distance between elements by two margins side by side.

## Shorthand Properties

- Some actually doesn't care the order, such as `border` as long as values are not the same properties.
- But some such as `margin` care the order.

## Content Box

- `box-sizing: border-box;` includes border and padding in the box model calculation, useful.

## Display

- `display-block` allow things to sit next to each other, but still allows you to style margin and padding easily, which is not possible for inline elements.
- `display: none` vs. `visibility: hidden`
  - Display none removes the element and does not block the position, so other elements can take its place instead.
  - Visibility hidden doesn't show the element, but the element keeps its place, so other elements cannot fill the empty spot.

## Block-Level Elements vs. Inline Elements

- Block-level elements take up all the available horizontal space.
  - `<div>`
- To inline elements, margin-top and margin-bottom have no effect.
- Width and height also won't have effect on inline elements.