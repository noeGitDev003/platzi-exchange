<template>
  <header class="shadow w-full">
    <nav>
      <nav
        class="flex items-center justify-between flex-wrap bg-green-light p-6"
      >
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <px-icon class="mr-2"></px-icon>
          <router-link
            :to="{ name: 'home' }"
            class="font-semibold text-xl text-white no-underline tracking-tight"
          >
            PlatziExchange
          </router-link>
        </div>
        <div
          class="hidden sm:block blok flex-grow lg:flex lg:items-center lg:wauto"
        >
          <div class="text-sm inline-flex lg:flex-grow">
            <router-link
              v-for="l in links"
              :key="l.title"
              :to="l.to"
              class="block lg:inline-block lg:mt-0 text-white no-underline hover:text-white hover:underline mr-4"
            >
              {{ l.title }}
            </router-link>
          </div>
        </div>
      </nav>
    </nav>
  </header>
</template>

<script>
import PxIcon from "@/components/PxIcon";

export default {
  name: "PxHeader",
  components: { PxIcon },

  props: {
    links: {
      type: Array,
      default: () => []
    }
  }
};
</script>
