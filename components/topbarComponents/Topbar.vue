<template>
<div class="ml-48 top-0 h-20 m-0 flex flex-col bg-white text-black font-semibold text-3xl shadow-sm justify-center pl-14">
    {{ pageName }}
</div>
</template>

<script>
export default {
    props: {
        pageName: {
            type: String,
            required: true
        }
    }    
}
</script>