<template>
<div class="w-screen h-screen">

    <topbar pageName="New Products"/>
    <div class="app-wrapper">
        <div class="flex flex-col ml-48 w-auto h-96 ">

            <label class="form-label">Product Name</label>
            <input v-model="productName" class=" mt-2 shadow appearance-none border rounded w-96 py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="How To Get The Warglaives of Azzinoth - Ebook" />

            <label class="form-label">Description</label>
            <textarea id="message" rows="4" class="mt-6  block p-2.5 w-96 text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Get ready to spend..."></textarea>

            <label class="form-label">Cover Image</label>
            <file-upload-zone fileName=""></file-upload-zone>

            <label class="form-label">Product File</label>
             <file-upload-zone fileName=""></file-upload-zone>

            <label class="form-label">Product Sample (Optional)</label>
             <file-upload-zone fileName=""></file-upload-zone>

            <label class="form-label">Price</label>
            <div class=" mt-6 flex w-96">
                <span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-l-md border border-r-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600">
                    $
                </span>
                <input v-model="productPrice" type="text" id="website-admin" class="rounded-none rounded-r-lg bg-gray-50 border text-gray-900 focus:ring-blue-500 focus:border-blue-500 block flex-1 text-sm border-gray-300 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="9.99">
            </div>

             <!--Component for the product url-->
            <label class="form-label">Product URL</label>
            <div class=" mt-6 flex w-96">
                <span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-l-md border border-r-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600">
                    https://flow/prod/
                </span>
                <input type="text" id="website-admin" class="rounded-none rounded-r-lg bg-gray-50 border text-gray-900 focus:ring-blue-500 focus:border-blue-500 block flex-1 text-sm border-gray-300 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="azzinoth-ebook">
            </div>

            <product-button class="pt-5" pageName="newProduct" buttonText="Create Product" @onClick="onUpload"/>

        </div>

        <product-preview-card :productName="productName" :productPrice="productPrice"></product-preview-card>
    </div>
</div>
</template>

<script>
import FileUploadZone from '../components/productComponents/FileUploadZone.vue'
import ProductPreviewCard from '../components/productComponents/ProductPreviewCard.vue'

export default {
  components: { FileUploadZone, ProductPreviewCard },
    data() {
        return {
            productName: "",
            productDescription: "",
            imagePath: "", 
            productPrice: "",
            isUserCoverImageUploaded: false,
            selectedCoverImage: null,
            selectedCoverImageName: "SVG, PNG, JPG or GIF (MAX. 800x400px)",
            selectedProductFile: null,
            selectedProductFileName: null,
            selectedProductSampleFile: null,
            selectedProductSampleFileName: null,
        }
    },
    methods: {
        onCoverImageSelected() {
            let input = this.$refs.fileInput
            let file = input.files
            if (file && file[0]) {
                let reader = new FileReader
                reader.onload = e => {
                    this.selectedCoverImage = e.target.result
                }
                reader.readAsDataURL(file[0])
                this.$emit('input', file[0])
            }
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