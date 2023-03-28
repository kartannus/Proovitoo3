<template>
  <div class="bg-white">
    <div class="bg-black">
      <div class="text-gray-400">Page</div>
    </div>
    &nbsp;
    <div class="flex justify-center mb-8"><img src="./assets/img/inbank.png" alt="Inbank"></div>
    <div class="absolute top-10 right-20 h-10 w-12"><svg fill="none" stroke="currentColor" stroke-width="1.5"
        viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <path stroke-linecap="round" stroke-linejoin="round"
          d="M10.5 6h9.75M10.5 6a1.5 1.5 0 11-3 0m3 0a1.5 1.5 0 10-3 0M3.75 6H7.5m3 12h9.75m-9.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-3.75 0H7.5m9-6h3.75m-3.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-9.75 0h9.75">
        </path>
      </svg></div>
    <div class="flex justify-center flex-wrap mr-10">
      <div class="relative">
        <img class="rectangle" src="./assets/img/rectangle.png" alt="Rectangle">
        <img class="cupcake absolute top-30 left-35 flex" src="./assets/img/cupcake.png" alt="Cupcake">
      </div>
      <div class="pl-36">
        <div class="grid gap-1 grid-cols-1 grid-rows-2 text-center mt-12">
          <span class="text-4xl">Good news!</span>
          <span class="text-lg text-gray-500">Your loan has been approved</span>
        </div>
        &nbsp;
        <div class="border-t-1 border border-gray-130"></div>
        &nbsp;
        <div
          class="grid items-end gap-y-10 grid-cols-2 grid-rows-3 text-center text-gray-500 px-2 border-gray-200 h-32 justify-center">
          <span>Personal loan offer</span>
          <span class="text-black text-lg">1,700.00 €</span>
          <span>Loan period</span>
          <span class="text-black text-lg">36 months</span>
          <span>Monthly payment</span>
          <span class="text-black text-lg">92.27%</span>
        </div>
        &nbsp;
        <div class="border-t-1 border border-gray-130"></div>
        &nbsp;
        <div class="grid gap-10 grid-cols-2 grid-rows-2 text-center text-gray-500 border-gray-500 mb-7">
          <span>Interest rate</span>
          <span class="text-black text-lg">12.90%</span>
          <span>Margin</span>
          <span class="text-black text-lg">8.90% + 6 months EURIBOR (0%)</span>
        </div>
        <div class="border-t-1 border border-gray-130 text-center border-gray-200"></div>
        &nbsp;
        <div class="flex items-center justify-center text-gray-500 text-center">
          <svg fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
            aria-hidden="true" style="width: 20; height: 20;">
            <path stroke-linecap="round" stroke-linejoin="round"
              d="M9 12.75L11.25 15 15 9.75M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
          </svg>
          &nbsp; Promo code applied
        </div>
        &nbsp;
        <div class="border-t-1 border border-gray-130"></div>
        &nbsp;
        <div class="grid grid-cols-1 grid-rows-2 gap-5">
          <button class=" btn rounded bg-purple-900 text-white cursor-pointer">View offer details</button>
          <div class>
            <Popup :is-open="popupOpen" @close="popupOpen = false">
            </Popup>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import Popup from './components/Popup.vue';


export default {
  components: {
    Popup
  },
  data() {
    return {
      popupOpen: false
    };
  },
  methods: {
    showPopup() {
      this.popupOpen = true;
    }
  }
};
</script>
