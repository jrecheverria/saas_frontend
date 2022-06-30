<template>
<div class="w-screen h-screen">

    <topbar pageName="New Products"/>
    <div class="ml-14 flex flex-row">
        <div class="flex flex-col ml-48 w-auto h-96 ">
            <label class=" mt-6 text-gray-600 text-sm font-semibold">Product Name</label>
            <input v-model="productName" class=" mt-2 shadow appearance-none border rounded w-96 py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="How To Get The Warglaives of Azzinoth - Ebook" />

            <label class=" mt-6 text-gray-600 text-sm font-semibold">Description</label>
            <textarea id="message" rows="4" class="mt-6  block p-2.5 w-96 text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Get ready to spend..."></textarea>

            <label class=" mt-6 text-gray-600 text-sm font-semibold">Cover Image</label>
            <div class=" mt-6 flex justify-center items-center w-96 shadow-lg">
                <label for="dropzone-file" class="flex flex-col justify-center items-center w-full h-44 bg-gray-50 rounded-lg border-2 border-gray-300 border-dashed cursor-pointer dark:hover:bg-bray-800 dark:bg-gray-700 hover:bg-gray-100 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600">
                    <div class="flex flex-col justify-center items-center pt-5 pb-6">
                        <svg class="mb-3 w-10 h-10 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"></path></svg>
                        <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                        <p class="text-xs text-gray-500 dark:text-gray-400">{{ selectedCoverImageName }}</p>
                    </div>
                    <input id="dropzone-file" type="file" class="hidden" @change="onCoverImageSelected"/>
                </label>
            </div> 

            <label class=" mt-6 text-gray-600 text-sm font-semibold">Product File</label>
            <div class=" mt-6 flex justify-center items-center w-96 shadow-lg">
                <label for="dropzone-file" class="flex flex-col justify-center items-center w-full h-44 bg-gray-50 rounded-lg border-2 border-gray-300 border-dashed cursor-pointer dark:hover:bg-bray-800 dark:bg-gray-700 hover:bg-gray-100 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600">
                    <div class="flex flex-col justify-center items-center pt-5 pb-6">
                        <svg class="mb-3 w-10 h-10 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"></path></svg>
                        <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                        <p class="text-xs text-gray-500 dark:text-gray-400">SVG, PNG, JPG or GIF (MAX. 800x400px)</p>
                    </div>
                    <input id="dropzone-file" type="file" class="hidden" @change="onProductFileSelected"/>
                </label>
            </div> 

            <label class=" mt-6 text-gray-600 text-sm font-semibold">Product Sample (Optional)</label>
            <div class=" mt-6 flex justify-center items-center w-96 shadow-lg">
                <label for="dropzone-file" class="flex flex-col justify-center items-center w-full h-44 bg-gray-50 rounded-lg border-2 border-gray-300 border-dashed cursor-pointer dark:hover:bg-bray-800 dark:bg-gray-700 hover:bg-gray-100 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600">
                    <div class="flex flex-col justify-center items-center pt-5 pb-6">
                        <svg class="mb-3 w-10 h-10 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"></path></svg>
                        <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                        <p class="text-xs text-gray-500 dark:text-gray-400">SVG, PNG, JPG or GIF (MAX. 800x400px)</p>
                    </div>
                    <input id="dropzone-file" type="file" class="hidden" @change="onProductSampleFileSelected"/>
                </label>
            </div> 

            <label class=" mt-6 text-gray-600 text-sm font-semibold">Price</label>
            <div class=" mt-6 flex w-96">
                <span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-l-md border border-r-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600">
                    $
                </span>
                <input v-model="productPrice" type="text" id="website-admin" class="rounded-none rounded-r-lg bg-gray-50 border text-gray-900 focus:ring-blue-500 focus:border-blue-500 block flex-1 text-sm border-gray-300 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="9.99">
            </div>


            <label class=" mt-6 text-gray-600 text-sm font-semibold">Product URL</label>
            <div class=" mt-6 flex w-96">
                <span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-l-md border border-r-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600">
                    https://flow/prod/
                </span>
                <input type="text" id="website-admin" class="rounded-none rounded-r-lg bg-gray-50 border text-gray-900 focus:ring-blue-500 focus:border-blue-500 block flex-1 text-sm border-gray-300 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="azzinoth-ebook">
            </div>
            <product-button class="pt-5" pageName="newProduct" buttonText="Create Product" @onClick="onUpload"/>

        </div>

        <div class="max-w-lg bg-white rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700 ml-20 mt-5">
            <a href="#">
                <img class="rounded-t-lg" :src="require(`../static/product-template-image.png`)" alt="" />
            </a>
            <div class="p-5">
                <a href="#">
                    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ productName }}</h5>
                </a>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">$ {{ productPrice }}</p>
                <a href="#" class="inline-flex items-center py-2 px-3 text-sm font-medium text-center text-white bg-primary rounded-lg hover:bg-selected focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                    Buy
                    <svg class="ml-2 -mr-1 w-4 h-4" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                </a>
             </div>
        </div>
    </div>
</div>
</template>

<script>

export default {
    data() {
        return {
            productName: "",
            productDescription: "",
            imagePath: "", 
            productPrice: "",
            selectedCoverImage: "../static/product-template-image.png",
            selectedCoverImageName: "SVG, PNG, JPG or GIF (MAX. 800x400px)",
            selectedProductFile: null,
            selectedProductFileName: null,
            selectedProductSampleFile: null,
            selectedProductSampleFileName: null,
        }
    },
    methods: {
        onCoverImageSelected(event) {
            console.log(event)
            this.selectedCoverImage = event.target.files[0]
            this.selectedCoverImageName = event.target.files[0].name
        },
        onProductFileSelected(event) {
            console.log(event)
            this.selectedProductFile = event.target.files[0]
            this.selectedProductFileName = event.target.files[0].name
        },
        onProductSampleFileSelected(event) {
            console.log(event)
            this.selectedProductSampleFile = event.target.files[0]
             this.selectedProductSampleFileName = event.target.files[0].name
        },
        onUpload() {
            axios.post()
        }
    }
}
</script>