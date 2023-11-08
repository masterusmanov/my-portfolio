<script setup>
    // const data3 = await useFetch('http://localhost:1987/api/workplace')
    const data3 = await useFetch('https://masterusmanov.onrender.com/api/workplace')

    console.log(data3.data._rawValue);


</script>

<template>
   <Backbtn/>
  <section class="flex pb-24">
    <div class="mx-auto mt-10 w-[1200px]">
      <h1 class="text-4xl font-bold">Workplace</h1>
      <div class="flex flex-wrap mt-10 justify-beetwen items-center gap-6">
          <div v-for="el in data3.data._rawValue" :key="el.id" class="text-justify shadow-lg shadow-gray-500 p-5">
              <h1 class="font-bold text-2xl pt-5"><b class="text-red-600">Company name: </b><span> {{el.company}}</span></h1>
              <h1 class="font-bold text-2xl pt-5"><b class="text-red-600">Position: </b><span> {{el.position}}</span></h1>
              <h1 class="font-bold text-2xl pt-5"><b class="text-red-600">Working times: </b><span> {{el.start_date}}</span></h1>
            </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
