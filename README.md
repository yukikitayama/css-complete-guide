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

## !important

**Overwrites** specifity and all other selectors. But don't use this most cases, because the CSS code will be messy.

## :not() selector

It's interesting, but the CSS code will be messy, so better to avoid.

## Positioning

By default, position: uses static. But by changing it, such as absolute, relative, fixed, sticky, we can change the positions of elements in webpage.

**Document flow**

**Positioning context** is, such as the element itself, viewport, parent elements, what does my position changes refer to?

`position: fixed;` will remove the element from document flow, so other elements will take over the original position. And change it from block element to inline element style. This refers `viewport`.

**z-index** works only when the element is using `position` value except static default. For example `position: fixed;` and `z-index: -1;

`position: absolute;` changed to closest ancestor which has position property. 
`position: relative;` 

Parent is `position: relative;` and child is `position: absolute;`

If you use no parent and only child with relative position, child moves to the new position relative from the original position.

- [How to set an image's width and height without stretching it?](https://stackoverflow.com/questions/1733006/how-to-set-an-images-width-and-height-without-stretching-it)

`position: sticky;` sticky continues until its parent ends. But sticky is not perfect in browser support.

### Stacking Context

`z-index` doesn't solely decide the stacking. z-index order of parent affect its children.

## Style Image

If you enter `img` tag, default height and width of the image file is used, no matter what height and width of the surrounding elements.

`height: 100%;` in `img` CSS also leads to the original height of the image file, not height defined by the container.

The container needs to specify height and width and set `display: inline-block;`, and use `height: 100%;` in `img`.

`img` CSS can use `width: 100%;` and `display: block;`.

`filter: ;` is to apply basic effect to images, such as grayscale and blur.

## Size and unit

`rem` and `em` about font size.

`vh` and `vw`

### Percentage %

**containing block** is a parent element which has a certain width or height. Its children can use % of this containing block.

1. Elements using `position: fixed;` refer to `viewport` to calculate `%`.

2. Elements with `position: absolute` refer to `ancestor/content` plus padding to calculate `%`. And the referred elements have `position: absolute;`, `position: relative;`, `position: fixed;`, or `position: sticky;`.

3. Elements with `position: static;` or `position: relative;` refer to `ancestor/content` without padding to calculate `%`. Ancestor is the closest ancestor with **block level element**.

`height: 100%;` is tricky. Without `position: absolute;`, it won't work, even if `width: 100%;` works.

## !important

Rarely use `!important`. It's a bad practice to often use, because it breaks the specificity. You could use to overwrite the effect of their party library.

## em

Font-size will depend on the font-size of browser. 

But em multiplication will be accumulated by inheritance.

## rem

Just take the font size of the browser and multiply the rem number applied to the element. 

**No accumulation in inheritance**.

Maybe using rem is more likely.

em and rem can be applied to font-size, margin, padding.

Use em and rem to make sizes dynamic to browser font size changes. Maybe we don't wanna apply em and rem to border and box-shadow.

## Unit Recommendation

- Root element font-size
  - `%` percentage of the browser setting.
- font-size except root element
  - `rem` (relative to root font-size)
- Padding and margin
  - `rem`
- Border
  - `px`
- Width and height
  - `%`, `vw`, `vh`
- Top and bottom, left and right
  - `%`

## Center Elements

`margin: auto`, but it only works for `block level` elements with `explicitly width` assigned
