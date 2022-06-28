<template>
    <router-link :to="`/${pageName}`">
        <div class="sidebar-item group">
            <!-- Not sure why this grouping isnt working -->
            <!-- <span class="sidebar-indicator group-hove:scale-100"></span> -->
            {{ pageName }}
        </div>
    </router-link>
    
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

