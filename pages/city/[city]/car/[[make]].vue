<template>
  <div>
    <NavBar />
    <div
      class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg: px-16 pb-16 w-3/5"
    >
      <div class="mt-32 flex">
        <CarSideBar />

        <!-- CARS CARDS -->
        <div class="w-full">
          <!-- CAR CARD -->
          <div
            class="shadow border w-full overflow-hidden mb-5 cursor-pointer h-[200px]"
          >
            <div class="flex h-full">
              <img
                src="https://www.topgear.com/sites/default/files/2022/07/6_0.jpg"
                alt="a blue car"
                class="w-[350px] h-full"
              />
              <div class="p-4 flex flex-col">
                <div>
                  <h1 class="text-2xl text-blue-700">bentley</h1>
                  <p class="text-gray-700">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  </p>
                </div>
                <h1 class="mt-auto text-xl">$60,000</h1>
              </div>
            </div>
          </div>
          <!-- CAR CARD -->
        </div>
        <!-- CARS CARDS -->
      </div>
    </div>
    <!-- CARS PAGE -->
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
