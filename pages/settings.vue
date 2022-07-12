<template>
  <div class="flex flex-col items-center bg-gray-200 h-screen justify-center">
    <form action="" class="bg-white rounded-2xl mx-8 my-8 py-2 px-4">
      <div class="flex flex-row my-5 mx-auto">
        <div class="flex flex-col mr-3">
          <div class="settings-label">First Name</div>
          <input class="settings-item" v-model="firstName" placeholder="John" />
        </div>
        <div class="flex flex-col ml-3">
          <div class="settings-label">Last Name</div>
          <input class="settings-item" v-model="lastName" placeholder="Smith" />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col w-full">
          <div class="settings-label">Email</div>
          <input
            class="settings-item w-full"
            v-model="email"
            placeholder="john.smith@gmail.com"
          />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col w-full">
          <div class="settings-label">Phone #</div>
          <input
            class="settings-item w-full"
            v-model="phone"
            placeholder="123-456-7890"
          />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col w-full">
          <div class="settings-label">Address</div>
          <input
            class="settings-item w-full"
            v-model="address"
            placeholder="123 ABC Drive"
          />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col mr-3">
          <div class="settings-label">City</div>
          <input class="settings-item" v-model="city" placeholder="Seattle" />
        </div>
        <div class="flex flex-col ml-3">
          <div class="settings-label">State</div>
          <input class="settings-item" v-model="state" placeholder="Washington" />
        </div>
      </div>
      <div class="flex flex-row my-5">
        <div class="flex flex-col mr-3">
          <div class="settings-label">Zip</div>
          <input class="settings-item" v-model="zip" placeholder="10001" />
        </div>
        <div class="flex flex-col ml-3">
          <div class="settings-label">Country</div>
          <input class="settings-item" v-model="country" placeholder="USA" />
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