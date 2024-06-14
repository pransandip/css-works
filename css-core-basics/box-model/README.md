# The CSS Box Model

In CSS, the term `box model` is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: \
`content`, `padding`, `borders` and `margins`. The image below illustrates the box model:

<img alt="box-model-img" src="https://github.com/pransandip/css-works/blob/main/css-core-basics/box-model/img/box-model.png?raw=true" width=800 height=360>

### Explanation of the different parts :

- _Content_ - The content of the box, where text and images appear
- _Padding_ - Clears an area around the content. The padding is transparent
- _Border_ - A border that goes around the padding and content
- _Margin_ - Clears an area outside the border. The margin is transparent

#### The box model allows us to add a border around elements, and to define space between elements.

### Example :

_Demonstration of the box model :_

```
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```

# color-scheme

The `color-scheme` CSS property allows an element to indicate which color schemes it can comfortably be rendered in

Common choices for operating system color schemes are `light` and `dark`, or `day mode` and `night mode`. When a user selects one of these color schemes, the operating system makes adjustments to the user interface. This includes form `controls`, `scrollbars`, and the used values of `CSS system colors`.

### Examples :

_**Declaring color scheme preferences**_

To opt the entire page into the user's color scheme preferences, declare `color-scheme` on the `:root` element.

```
:root {
  color-scheme: light dark;
}
```

To opt in specific elements to the user's color scheme preferences, declare `color-scheme` on those elements.

```
header {
  color-scheme: only light;
}
main {
  color-scheme: light dark;
}
footer {
  color-scheme: only dark;
}
```

#### To style elements based on color scheme preferences, use the `prefers-color-scheme` media query.

```
:root {
  color-scheme: light dark;
}

@media (prefers-color-scheme: light) {
  .element {
    color: black;
    background-color: white;
  }
}

@media (prefers-color-scheme: dark) {
  .element {
    color: white;
    background-color: black;
  }
}
```

#### To know more go [click here.](https://developer.mozilla.org/en-US/docs/Web/CSS/color-schemes)
