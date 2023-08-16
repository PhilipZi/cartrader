<template>
  <div>
    <div class="mt-32 flex">
      <NuxtErrorBoundary>
        <CarSideBar />
        <NuxtPage />
        <template #error="{ error }">
          <div class="text-center mx-auto flex flex-col">
            <h1 class="text-red-600 text-4xl mb-4">
              Sorry, somthing went wrong
            </h1>
            <code>{{ error }}</code>
            <button
              class="text-white bg-blue-400 px-10 py-3 rounded mt-4"
              @click.prevent="error.value = null"
            >
              Go back
            </button>
          </div>
        </template>
      </NuxtErrorBoundary>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
const { toTitleCase } = useUtilities();

useHead({
  title: `${
    route.params.make ? toTitleCase(route.params.make) : "Cars"
  } in ${toTitleCase(route.params.city)}`,
  meta: [
    {
      hid: "description",
      name: "description",
      content: "Car",
    },
  ],
});

definePageMeta({
  layout: "custom",
});
</script>
