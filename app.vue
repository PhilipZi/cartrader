<template>
  <div>
    <header
      class="sticky top-0 z-50 flex justify-between items-center space-x-1 border-b bg-white p-4 shadow-md"
    >
      <a class="text-3xl font-mono" href="">Cartrader</a>
    </header>

    <!-- CAR DETAIL PAGE -->
    <div
      class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg: px-16 pb-16 w-3/5"
    >
      <div>
        <!-- CAR HERO -->

        <div class="mt-10">
          <img
            src="https://www.topgear.com/sites/default/files/2022/07/6_0.jpg"
            class="w-full"
            alt="bentley"
          />
          <h1 class="mt-10 text-4xl">Bentley</h1>
          <div
            class="text-slate-500 flex text-lg mt-3 border-b pb-5 justify-between"
          >
            <div class="flex">
              <p class="mr-2">5 Seats</p>
              <p class="mr-2">|</p>
              <p class="mr-2">67,454 Miles</p>
            </div>
            <div>
              <p class="font-bold text-2xl">$24,555</p>
            </div>
          </div>
        </div>
      </div>
      <!-- CAR HERO -->
      <!-- CAR ATTRIBUTES -->
      <div class="mr-10 mt-5 border-b pb-5">
        <div class="flex text-lg mt-2">
          <p class="rounded text-lime-800 mr-3">✔</p>
          <p>Leather Interior</p>
        </div>
      </div>
      <!-- CAR ATTRIBUTES -->
    </div>
    <!-- CAR DETAIL PAGE -->
  </div>
</template>
