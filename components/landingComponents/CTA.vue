<template>
    <section class="py-0 bg-white sm:py-16 lg:py-24">
        <div class="px-4 mx-auto sm:px-6 lg:px-8 max-w-7xl">
            <div class="text-center">
                <h2 class="text-3xl font-bold leading-tight text-black sm:text-4xl lg:text-5xl">Get full access to {{companyName}}</h2>
                <p class="mt-4 text-2xl font-medium">Sign Up Today and Start Tracking Your Wallet in a Whole New Way</p>

                <div class="flex flex-col items-center justify-center px-16 mt-8 space-y-4 sm:space-y-0 sm:space-x-4 sm:flex-row lg:mt-12 sm:px-0">
                    <NuxtLink to="/signup" title="" class="inline-flex items-center justify-center w-full px-8 py-4 text-base font-semibold text-white transition-all duration-200 bg-indigo-600 border border-transparent rounded-md sm:w-auto hover:bg-indigo-700 focus:bg-indigo-700" role="button"> Try For Free </NuxtLink>
                    <NuxtLink to="/pricing" title="" class="inline-flex items-center justify-center w-full px-8 py-4 text-base font-semibold text-black transition-all duration-200 bg-white border rounded-md sm:w-auto" role="button"> Pricing Plans </NuxtLink>
                </div>

                <p class="mt-6 text-base text-black">Already have an account? <NuxtLink to="/login" title="" class="text-indigo-600 transition-all duration-200 hover:text-indigo-700 focus:text-indigo-700 hover:underline">Log in</NuxtLink></p>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'CallToAction',
        data() {
            return {
                companyName: process.env.VUE_APP_COMPANY_NAME,
            }
        },
        methods: {
            //
        }
    }
</script>