# Matestack Core Component: Dl

The HTML `<dl>` tag, implemented in Ruby.

## Parameters
This component can take various optional configuration params and either yield content or display what gets passed to the `text` configuration param.

### Text (optional)
Expects a string which will be displayed as the content inside the `<dl>` tag.

### HMTL attributes (optional)
This component accepts all the canonical [HTML global attributes](https://www.w3schools.com/tags/ref_standardattributes.asp) like `id` or `class`.

## Examples

### Example 1: Yield a given block

```ruby
dl id: "foo", class: "bar" do
  dt text: "dt component"
  dd text: "dd component"
end
```

returns

```html
<dl id="foo" class="bar">
  <dt>dt component</dt>
  <dd>dd component</dd>
</dl>
```

### Example 2: Render options[:text] param

```ruby
dl id: "foo", class: "bar", text: 'Hello World'
```

returns

```html
<dl id="foo" class="bar">
  Hello World
</dl>
```
