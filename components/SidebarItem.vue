<template>
    <router-link :to="`/${pageName}`">
        <div class="relative flex 
                items-center justify-center 
                h-12 w-32 mt-3 mb-3 mx-auto
                hover:shadow-lg bg-inherit
                text-primary
               hover:bg-primary hover:text-white
               rounded-2xl hover:rounded-xl
               transition-all duration-300">
            {{ sideBarItemText }}    
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
        sideBarItemText: {
            type: String,
            required: true
        }
    }
}
</script>

