<template>
<h1>Class Binding</h1>
<h1 :class="applyStyle">Home Component</h1>
<button v-on:click="colorfull=!colorfull">Apply Style</button>
</template>

<script>
export default {
    name: 'HomePage',
    data() {
        return {
            colorfull: false,
        }
    },
    computed: {
        applyStyle() {
            return {
                green: this.colorfull,
                err: true,
                other:true,
            }
        }
    }
}
</script>

<style scoped>
h1 {
    color: orange;
}

.green {
    background-color: grey;
}

.err {
    color: red;
}
.other{
  font-size: 20px;
}
</style>
