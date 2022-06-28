<template>
  <div>
    <div class="overflow-x-hidden bg-white">
      <section class="relative py-6 sm:py-6 lg:pt-12 lg:pb-12">
        <div class="px-4 mx-auto sm:px-6 lg:px-8 max-w-7xl">
          <div
            class="
              grid grid-cols-1
              gap-y-8
              lg:items-center lg:grid-cols-2
              xl:grid-cols-5
            "
          >
            <div
              class="text-center xl:col-span-2 lg:text-left sm:px-8 md:px-16 lg:px-0"
            >
              <div class="max-w-sm mx-auto sm:max-w-full md:max-w-full">
                <h1
                  class="
                    text-4xl
                    font-bold
                    leading-tight
                    text-gray-900
                    sm:text-5xl sm:leading-tight
                    lg:text-6xl lg:leading-tight
                    font-pj
                  "
                >
                  Start selling today in 60 seconds or less.
                </h1>

            

          
              </div>

              <div
                class="
                  mt-8
                  sm:flex sm:items-center sm:justify-center
                  lg:justify-start
                  sm:space-x-5
                  lg:mt-12
                "
              >
                <NuxtLink
                  to="/signup"
                  title=""
                  class="
                    inline-flex
                    items-center
                    justify-center
                    px-8
                    py-4
                    text-lg
                    font-bold
                    text-white
                    transition-all
                    duration-200
                    bg-gray-900
                    border border-transparent
                    rounded-xl
                    focus:outline-none
                    focus:ring-2
                    focus:ring-offset-2
                    focus:ring-gray-900
                    font-pj
                    hover:bg-gray-600
                  "
                  role="button"
                >
                  Sign Up
                </NuxtLink>

                <a
                  href="/dashboard"
                  title=""
                  class="
                    inline-flex
                    items-center
                    justify-center
                    px-4
                    py-4
                    mt-4
                    text-lg
                    font-bold
                    transition-all
                    duration-200
                    bg-transparent
                    border border-transparent
                    sm:mt-0
                    font-pj
                    rounded-xl
                    focus:outline-none
                    focus:ring-2
                    focus:ring-offset-2
                    focus:ring-gray-300
                    hover:bg-gray-200
                    focus:bg-gray-200
                  "
                  role="button"
                >
                  <svg
                    class="w-5 h-5 mr-2"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"
                    />
                  </svg>

                  Live Demo
                </a>
              </div>
            </div>

            <div class="xl:col-span-3">
              <img
                class="w-full mx-auto transform scale-110"
                src="https://cdn.rareblocks.xyz/collection/clarity/images/hero/2/illustration.png"
                alt=""
              />
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
}
</script>

<style>
</style>