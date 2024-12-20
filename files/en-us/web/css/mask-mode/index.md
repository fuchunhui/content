---
title: mask-mode
slug: Web/CSS/mask-mode
page-type: css-property
browser-compat: css.properties.mask-mode
---

{{CSSRef}}

The **`mask-mode`** [CSS](/en-US/docs/Web/CSS) property sets whether the mask reference defined by {{cssxref("mask-image")}} is treated as a luminance or alpha mask.

## Syntax

```css
/* Keyword values */
mask-mode: alpha;
mask-mode: luminance;
mask-mode: match-source;

/* Multiple values */
mask-mode: alpha, match-source;

/* Global values */
mask-mode: inherit;
mask-mode: initial;
mask-mode: revert;
mask-mode: revert-layer;
mask-mode: unset;
```

The `mask-mode` property is specified as one or more of the keyword values listed below, separated by commas.

### Values

- `alpha`
  - : This keyword indicates that the transparency (alpha channel) values of the mask layer image should be used as the mask values.
- `luminance`
  - : This keyword indicates that the luminance values of the mask layer image should be used as the mask values.
- `match-source`

  - : If the {{cssxref("mask-image")}} property is of type `<mask-source>`, the luminance values of the mask layer image should be used as the mask values.

    If it is of type {{cssxref("&lt;image&gt;")}}, the alpha values of the mask layer image should be used as the mask values.

## Formal definition

{{cssinfo}}

## Formal syntax

{{csssyntax}}

## Examples

### Using alpha mask mode

```html live-sample___mask-mode-example
<div class="masked"></div>
```

```css live-sample___mask-mode-example
.masked {
  width: 227px;
  height: 200px;
  background: blue linear-gradient(red, blue);

  mask-image: url(https://mdn.github.io/shared-assets/images/examples/mdn.svg);
  mask-mode: alpha;
}
```

{{EmbedLiveSample("mask-mode-example", "", "250px")}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Clipping and Masking in CSS](https://css-tricks.com/clipping-masking-css/)
