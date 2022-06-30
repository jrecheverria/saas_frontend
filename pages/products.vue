<template>
<div class="w-screen h-screen">
    <topbar pageName="Products"/>

    <div class="flex flex-col ml-48 w-auto h-96 items-center justify-center">
        <div class="flex flex-col bg-white w-72 h-auto justify-start items-start">
            <img class="w-10 h-10 mb-5" src="../static/icons8-impossible-shapes-100.png"/>
            <p class="text-left text-gray-600">
                Products are what you sell to customers. It can be any digital good from an e-book to art and music. Go ahead and list your first product!
            </p>
            <product-button class="pt-5" pageName="newProduct" buttonText="Add A Product"/>
        </div>
        
    </div>
</div>
</template>

<script>

export default {

}
</script>
