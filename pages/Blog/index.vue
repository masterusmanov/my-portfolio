<script setup>

// const data4 = await useFetch('http://localhost:1987/api/blog')
const data4 = await useFetch('https://masterusmanov.onrender.com/api/blog')
console.log(data4.data._rawValue);


</script>

<template>
    <Backbtn/>
  <section class="flex pb-24">
    <div class="mx-auto mt-10 w-[1200px]">
      <h1 class="text-4xl font-bold">Blog</h1>
      <div v-for="el in data4.data._rawValue" :key="el.id" class="flex justify-beetwen items-center gap-6 mt-10">
        <div class="w-[30%]">
            <img :src="el.img_link" alt="Blog" class="rounded-xl">
        </div>
        <div class="w-[100%] text-justify p-4 pt-14 border-b border-gray-500">
            <h1 class="font-bold text-2xl pt-5">{{ el.title }}</h1>
            <p class="pt-4 text-xl pb-5">{{el.content}}</p>
            <p class="pt-4 font-bold text-right">{{ new Date().getDay()+18 }}.{{ new Date().getMonth()+1}}.{{new Date().getFullYear()}}</p>
          </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
