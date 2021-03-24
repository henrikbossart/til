# Handle multiple instances of components and IDs

To avoid duplicate IDs on pages where a component is used several times, do the following:

```JavaScript
<script lang="ts">
let instanceId = 0;

export default defineComponent({
  name: "ComponentName",
  setup() {
    instanceId++;
  }
});
</script>

```
```JavaScript
<table :id="`table-${instanceId}`" />
```