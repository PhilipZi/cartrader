<template>
  <div>
    <CarDetailHero />
    <CarAttributes />
    <CarDescription />
    <CarContact />
  </div>
</template>

<script setup>
const route = useRoute();
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

definePageMeta({
  layout: "custom",
});
</script>
