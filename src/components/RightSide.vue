<template >
    <div class="rightside">
        <div class="flex justify-center py-14">
  <div class="mb-3 sm:w-50">
    <div class="input-group relative flex flex-wrap items-stretch w-full mb-4 rounded">
      <input type="search" class="form-control relative flex-auto min-w-0 block w-full px-3 py-1.5 text-base font-normal text-gray-700 bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0 focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" placeholder="Search" aria-label="Search" aria-describedby="button-addon2">
      <span class="input-group-text flex items-center px-3 py-1.5 text-base font-normal text-gray-700 text-center whitespace-nowrap rounded" id="basic-addon2">

      </span>
    </div>
  </div>
</div>
<h1 class="py-7">Popular Movies</h1>
    <ul>
        <li>daa</li>
        <button type="button" class="inline-block px-6 py-2.5 bg-red-600 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-red-700 hover:shadow-lg focus:bg-red-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-red-800 active:shadow-lg transition duration-150 ease-in-out">See More</button>
    </ul>
    <h1 class="py-7">Favourites</h1>
    <ul>
        <li>grr</li>
        <button type="button" class="inline-block px-6 py-2.5 bg-red-600 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-red-700 hover:shadow-lg focus:bg-red-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-red-800 active:shadow-lg transition duration-150 ease-in-out">See More</button>
    </ul>
    </div>
</template>

<script>
export default {
name: 'RightSide',

    data() {
      return {
        listItems: []
      }
    },
    methods: {
      async getData() {
        const res = await fetch("https://api.themoviedb.org/3/movie/550?api_key=9a6631015d37456e3276b3ca5facf54d");
        const finalRes = await res.json();
        this.listItems = finalRes;
        console.log(this.listItems)
      }
    },
    mounted() {
      this.getData()
    }
  }
</script>

<style>
    .rightside{
        display: flex;
        flex-direction: column;
        width: 23vw;
        border-left: 2px solid #F3F3F3;
    }
</style>
