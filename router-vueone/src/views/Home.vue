<template>
  <div class="flex flex-wrap -mx-4">
    <div v-for="university in universities" class="w-1/3 px-4 mt-6">
      <div class="border p-4 border-gray-200 h-full">
        <h2 class="font-bold mb-3 text-lg">{{university.name}} </h2>
          <p class="mb-3">Country:{{university.country}}</p>
        <p><a target="_blank" :href="university.web_pages" ></a><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 008.716-6.747M12 21a9.004 9.004 0 01-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 017.843 4.582M12 3a8.997 8.997 0 00-7.843 4.582m15.686 0A11.953 11.953 0 0112 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0121 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0112 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 013 12c0-1.605.42-3.113 1.157-4.418" />
        </svg>


        </p>



      </div>

    </div>

  </div>

</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      universities:[]
    }

  },
  mounted(){
    fetch("http://universities.hipolabs.com/search?country=Bangladesh")
        .then(response => response.json()).then(json =>this.universities =json);
    // console.log(json)
  }
}
</script>

<style scoped>

</style>