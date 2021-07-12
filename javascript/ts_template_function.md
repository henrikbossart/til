# Handling an event in a Vue template without the need for creating a function

To avoid duplicate IDs on pages where a component is used several times, do the following:

```html
@input="event => {
  @ts-ignore
  $emit('update:modelValue', event?.target?.value);
}"

```