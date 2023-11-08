<template>
    <footer id="contacts" class="bg-teal-100">
        <div class="container mx-auto">
            <div class="py-10 grid justify-beetwen ml-10 items-center">
                <h3 class="text-[28px] font-bold text-blue-600">Contacts</h3>
                <h1 class="text-[48px] font-bold">Get in touch</h1>
                <p class="text-[20px] font-bold"><b>E-mail:</b> elyor.usmanov87@mail.ru <span class="text-red-600">&</span> <span>elyor.usmanov22@gmail.com</span></p>
                <p class="text-[20px] font-bold mt-3"><b>Phone number:</b> +998972179900 <span class="text-red-600">&</span> <span>+998950119900</span></p>
                <div class="flex justify-beetwen items-center gap-6 mt-5">
                    <a href="https://www.linkedin.com/in/elyor-usmanov-77016323b/"><img src="https://cdn-icons-png.flaticon.com/512/185/185964.png" alt="LinkedIn" class="w-[70px]"></a>
                    <a href="https://github.com/masterusmanov"><img src="https://cdn-icons-png.flaticon.com/512/25/25231.png" alt="GitHub" class="w-[70px]"></a>
                    <a href="https://t.me/masterusmanov"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Telegram_Messenger.png/800px-Telegram_Messenger.png" alt="Instagram" class="w-[75px]"></a>
                    <div  v-for="el in data2.data._rawValue" :key="el.id">
                        <a :href="el.social_network"><img :src="el.image_link" alt="Instagram" class="w-[75px]"></a>
                    </div>
                </div>
                <div class="pt-10 mt-10 text-[20px]">
                    <p>Copyright © {{new Date().getFullYear()}}. Develop & Designed by Usmanov Elyor</p>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>
    const data2 = await useFetch('http://localhost:1987/api/aboute-me')
</script>

<style lang="scss" scoped>

</style>