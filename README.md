# {LESS} Baseline

LESS mixin to apply a real baseline to your HTML&CSS content. Also comes with default styles for raw HTML5.

## Configuration

There are two basic values you can modify in the `config.less` file.

`@base-font-size` should be set to the smallest font-size is use (default: `13px`).<br/>
`@base-line-height` is the line-height for the vertical grid (default: `21px`).

## Usage

To apply the baseline invoke the `.baseline( <font-size>px )` mixin on **all** the elements which directly contain text. Also, all your vertical spacing between elements will need to be a multiple of `@base-line-height`.

### Example

```lessc
h1 {
  .baseline( @base-font-size * 3 );
}

h2 {
  .baseline( @base-font-size * 2 );
}

p {
  .baseline( @base-font-size );
  margin: @base-line-height 0;
}
```

Keep in mind the baseline is set by changing the vertical padding (and in special cases the top margin) of the elements.
