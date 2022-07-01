<template>
<div class="fixed top-0 left-0 h-screen w-48 m-0 flex flex-col bg-offWhite text-white shadow-lg items-center">
    <sidebar-item class="mt-20" pageName="products" iconName="house"/>
    <sidebar-item pageName="purchases" iconName="user"/>
    <sidebar-item pageName="sales" iconName="credit-card"/>
    <sidebar-item pageName="settings" iconName="gear"/>
    <button class="text-black" @click="onLogin">Click here to login</button>
</div>
</template>

<script>
export default {
  methods: {
    onLogin() {
        this.$auth.loginWith('auth0')
    }
  }
}
</script>
