<template>
  <div v-if="car">
    <CarDetailHero :car="car" />
    <CarAttributes :features="car.features" />
    <CarDescription :description="car.description" />
    <CarContact />
  </div>
</template>

<script setup>
const route = useRoute();
const { cars } = useCars();
const { toTitleCase } = useUtilities();

useHead({
  title: `${toTitleCase(route.params.name)} | Car Detail Page`,
  meta: [
    {
      name: "description",
      content: "Car Detail Page",
    },
  ],
});

const car = computed(() => {
  return cars.find((c) => c.id === parseInt(route.params.id));
});

definePageMeta({
  layout: "custom",
});
</script>
