<template>
    <h2>{{ yourName }}</h2>
    <h3>{{ yourAge }}</h3>
</template>
<script>
export default {
    props:{
        yourName: {
            type: String,
            required: true
        },
        yourAge:{
            type: Number,
            required: true
        }
    }
}
</script>