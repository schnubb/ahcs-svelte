<script>
  export let type;
  export let it;
  let label = "Absenden";
</script>

<button type="{type}" id="{id}">
    <slot name="label">
        {label}
    </slot>
</button>