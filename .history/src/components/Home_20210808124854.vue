<template>
    <h2 v-border:solid.round.shadow="{width:'5px',color: 'brown', shadow}">Home {{tmpDdata}}</h2>
</template>

<script>
export default {
    data() {
        return {
            tempData: "hello"
        }
    },
    directives : {
        border(el,binding) {
            // directivesの中ではthisが使えない
            // this.tempData = "変更しました"
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