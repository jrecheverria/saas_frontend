<template>
<router-link :to="`/${pageName}`">
    <div class="product-button group">
        {{ buttonText }}
    </div>
</router-link>
</template>

<script>

export default {
    props: {
        pageName: {
            type: String,
            required: true
        },
        buttonText: {
            type: String,
            required: true
        }
    }
}
</script>