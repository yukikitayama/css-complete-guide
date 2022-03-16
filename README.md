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

