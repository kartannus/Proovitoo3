<template>
  <div>
    <button class="btntwo w-rounded bg-white cursor-pointer semi-bold" @click="toggleModal = !toggleModal">
      Not interested
    </button>
    <div class="fixed inset-0 flex justify-center items-center z-50" v-if="toggleModal">
      <div class="bg-white rounded-xl w-96 h-auto px-5 py-4 flex flex-col">
        <button class="text-lg text-gray-300 hover:text-gray-900 cursor-pointer" @click="toggleModal = false">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
            class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
        &nbsp;
        <div class="text-lg text-left mt-4 px-3 text-gray-700 font-semibold">Help us improve!</div>
        <p class="text-sm text-left mt-2 mb-3 px-3 text-gray-600">We want to offer our clients the best experience. Your
          feedback will help us get better. You can select multiple answers.</p>
        <div class="flex flex-col items-start">
          <label class="inline-flex items-center text-center mb-6" v-for="(option, index) in options" :key="index">
            <input type="checkbox" class="form-checkbox" :value="option" v-model="selectedOptions">
            <span class="text-sm flex justify-center items-center">{{ option }}</span>
          </label>
        </div>
        <button class="btn" @click="toggleModal = false">
          Cancel loan application
        </button>
      </div>
    </div>
    <div v-if="toggleModal" class="fixed inset-0 backdrop-blur bg-opacity-25"></div>
  </div>
</template>
  
<script>
export default {
  name: "modal",
  data() {
    return {
      toggleModal: false,
      options: [
        "Loan amount is too small",
        "Interest is too high",
        "Not sure if I should take a loan",
        "I prefer another bank",
        "Option 5",
        "Timing is not right",
        "Other"
      ],
      selectedOptions: []
    };
  }
};
</script>

   
  
  