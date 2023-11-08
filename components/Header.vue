<template>
    <header class="sticky top-0 z-50 bg-teal-100 border-2 border-b-gray-400">
        <div class="container mx-auto h-[70px]">
            <div class="flex justify-beetwen items-center h-[70px]">
                <div class="w-1/2 flex items-center justify-beetwen ">
                    <h1 class="portfolioo text-[50px] font-semibold ml-5 text-yellow-400 ">
                        Port<span class="text-teal-900 font-semibold">folio</span>
                    </h1>
                </div>
                <div class="menu w-1/2 flex justify-end items-center font-bold gap-6 mr-5">
                    <a href="#aboute" class="hover:text-red-500">Home</a>
                    <a href="#aboute" class="hover:text-red-500">About</a>
                    <a href="#skills" class="hover:text-red-500">Skill</a>
                    <a href="#project" class="hover:text-red-500">Project</a>
                    <a href="/blog" class="hover:text-red-500">Blog</a>
                    <a href="/workplace" class="hover:text-red-500">Workplace</a>
                    <a href="#contacts" class="hover:text-red-500">Contact</a>
                </div>
            </div>
        </div>
    </header>
</template>

<script setup>
</script>

<style lang="scss" scoped>
    @media only screen and (max-width: 767px) {
        .portfolioo{
            display: none;
        }
        .menu{
            width: 100%;
            justify-content: center;
        }
    }
   
    @media only screen and (max-width: 548px) {
        .portfolioo{
            display: none;
        }
        .menu{
            width: 100%;
            justify-content: center;
            font-size: 11px;
            grid-gap: 15px;
            padding-left: 10px;
        }
    }
</style>
