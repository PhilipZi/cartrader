<template>
  <div class="shadow border w-64 mr-10 z-30 h-[190px]">
    <div class="p-5 flex justify-between relative cursor-pointer border-b">
      <h3>Location</h3>
      <h3
        @click.prevent="updateModal('location')"
        class="text-blue-400 capitalize"
      >
        {{ route.params.city }}
      </h3>
      <div
        class="absolute border shadow left-56 p-5 top-1 -m-1 bg-white"
        v-if="modal.location"
      >
        <input type="text" class="border p1 rounded" v-model="city" />
        <button
          @click.prevent="onChangeLocation"
          class="bg-blue-400 w-full mt-2 rounded text-white p-1"
        >
          Apply
        </button>
      </div>
    </div>
    <div class="p-5 flex justify-between relative cursor-pointer border-b">
      <h3>Make</h3>
      <h3 class="text-blue-400 capitalize">Any</h3>
    </div>
    <div class="p-5 flex justify-between relative cursor-pointer border-b">
      <h3>Price</h3>
      <h3 class="text-blue-400 capitalize">Any</h3>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();

const modal = ref({
  make: false,
  location: false,
  price: false,
});

const city = ref("");

const updateModal = (key) => {
  modal.value[key] = !modal.value[key];
};

const onChangeLocation = () => {
  if (!city.value) return;
  updateModal("location");
  navigateTo(`/city/${city.value}/car/${route.params.make}`);
  city.value = "";
};
</script>

<style scoped></style>
