<template>
  <div class="flex flex-col items-center bg-gray-300">
    <form action="" class="bg-white rounded-2xl mx-8 my-8 py-2 px-4">
      <div class="flex flex-row my-5 mx-auto">
        <div class="flex flex-col mr-3">
          <div class="mr-3">First Name</div>
          <input class="bg-gray-200" v-model="firstName" placeholder="John" />
        </div>
        <div class="flex flex-col ml-3">
          <div class="mr-3">Last Name</div>
          <input class="bg-gray-200" v-model="lastName" placeholder="Smith" />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col w-full">
          <div class="mr-3">Email</div>
          <input
            class="bg-gray-200 w-full"
            v-model="email"
            placeholder="john.smith@gmail.com"
          />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col w-full">
          <div class="mr-3">Phone #</div>
          <input
            class="bg-gray-200 w-full"
            v-model="phone"
            placeholder="123-456-7890"
          />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col w-full">
          <div class="mr-3">Address</div>
          <input
            class="bg-gray-200 w-full"
            v-model="address"
            placeholder="123 ABC Drive"
          />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col mr-3">
          <div class="mr-3">City</div>
          <input class="bg-gray-200" v-model="city" placeholder="Seattle" />
        </div>
        <div class="flex flex-col ml-3">
          <div class="mr-3">State</div>
          <input class="bg-gray-200" v-model="state" placeholder="Washington" />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col mr-3">
          <div class="mr-3">Zip</div>
          <input class="bg-gray-200" v-model="zip" placeholder="10001" />
        </div>
        <div class="flex flex-col ml-3">
          <div class="mr-3">Country</div>
          <input class="bg-gray-200" v-model="country" placeholder="USA" />
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "SettingsPage",
  layout: "app",
  data() {
    return {
      firstName: "",
    };
  },
  methods: {
    async updateUserDetails() {},
  },
};
</script>