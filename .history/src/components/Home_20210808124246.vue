<template>
    <h2 v-border:solid.round.shadow="{width:'5px',color: 'brown', shadow}">Home</h2>
</template>

<script>
export default {
    directives : {
        border(el,binding) {
            el.style.borderWidth = binding.value.width;
            el.style.borderColor = binding.value.color;
            el.style.borderStyle = binding.arg;
            if (binding.modifiers.shadow)
            {
                el.style.boxShadow = '0 2px 5px rgba(0,0,0,0.26)'
            }
        }
    }
}
</script>