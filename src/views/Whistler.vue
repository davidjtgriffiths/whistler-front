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
    </div>
    <div class="w-full mb-12 px-4">
      <card-table color="dark" />
    </div>
  </div>
</template>
<script>
import CardTable from "@/components/Cards/CardTable.vue";

export default {
  components: {
    CardTable,
  },
};
</script>
