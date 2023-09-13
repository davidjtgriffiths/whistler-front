<template>
  <div class="flex flex-wrap mt-4">
    <div class="w-full mb-12 px-4">
      <!-- Small Input -->
      <div class="mb-3 pt-0">
        <input type="text" placeholder="Small Input" class="px-2 py-1 placeholder-blueGray-300 text-blueGray-600 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"/>
      </div>
      <!-- Regular Input -->
      <div class="mb-3 pt-0">
        <input type="text" placeholder="Regular Input" class="px-3 py-3 placeholder-blueGray-300 text-blueGray-600 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"/>
      </div>
      <!-- Large Input -->
      <div class="mb-3 pt-0">
        <input type="text" placeholder="Large Input" class="px-3 py-4 placeholder-blueGray-300 text-blueGray-600 relative bg-white bg-white rounded text-base shadow outline-none focus:outline-none focus:shadow-outline w-full"/>
      </div>
      <button class="bg-emerald-500 text-white active:bg-emerald-600 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button">
        Small
      </button>
      <button class="bg-emerald-500 text-white active:bg-emerald-600 font-bold uppercase text-sm px-6 py-3 rounded shadow hover:shadow-lg outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button">
        Regular
      </button>
      <button
      @click.prevent="
                                        onSubmit()
                                    "
        class="bg-emerald-500 text-white active:bg-emerald-600 font-bold uppercase text-base px-8 py-3 rounded shadow-md hover:shadow-lg outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button">
        Large
      </button>
    </div>
    <div class="w-full mb-12 px-4">
      <card-table color="dark" />
    </div>
  </div>
</template>
<script setup>
/* eslint-disable */
import CardTable from "@/components/Cards/CardTable.vue";


  const onSubmit = async () => {
    console.log("kjashdjkahs askjdkla")
  }
</script>
