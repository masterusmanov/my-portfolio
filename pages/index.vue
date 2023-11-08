<template>
    <Header/>
    <section id="aboute" class="bg-teal-100 py-[100px]">
        <div class="container mx-auto py-10">
            <div class="hi flex jusrify-beetwen items-center ">
                <div class="about w-1/2 grid items-center justify-center pl-[100px]">
                    <div>
                        <p class="font-bold text-[24px]">Hi everyone, I am</p>
                    </div>
                    <div>
                        <h1 class="font-bold text-[48px]">Usmanov Elyor Elmuratovich</h1>
                    </div>
                    <div>
                        <p class="text-[20px]">I am a Full-stack (NodeJs+VueJs) developer</p>
                    </div>
                    <div class="flex justify-beetwen mt-10 items-center gap-10">
                        <a href="https://drive.google.com/file/d/1nyl_8Ku57QE2VloYURUvL5uOaF51seQs/view?usp=sharing" download class="py-4 px-8 text-xl bg-blue-400 text-white font-bold rounded-xl hover:bg-blue-600">Download CV</a>
                    </div>
                </div>
                <div class="myypic w-1/2 flex justify-center items-center font-bold">
                    <img src="../public/moy-e157806a.png" alt="" class="mypic rounded-full w-[400px] object-cover">
                </div>
            </div>
        </div>
    </section>
    <section class="py-10">
        <div class="container mx-auto">
            <div class="abc flex jusrify-beetwen items-center ">
                <div class="abpic w-1/2 grid items-center justify-beetwen">
                    <img src="../public/aboute.png" alt="" class="w-[500px] ">
                </div>
                <div class="about1 w-1/2 grid justify-beetwen items-center gap-6">
                    <div class="haq">
                        <p class="font-bold text-[24px] text-blue-500 font-bold">About</p>
                    </div>
                    <div>
                        <h1 class="font-bold text-[48px] font-bold">About myself</h1>
                    </div>
                    <div class="text">
                        <p class="text-[20px] text-justify">I am Usmanov Elyor Elmuratovich and was born in 1987. I studied in the "Foundation" and "Bootcamp Full-stack (NodeJS+VueJs)" courses at the "Najot Ta'lim" educational center.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section id="skills" class="bg-teal-100 py-10">
        <div class="container mx-auto ">
            <div class="grid jusrify-beetwen items-center ">
                <div class=" grid items-center justify-center">
                    <p class="font-bold text-[24px] text-blue-500 font-bold text-center">Skills</p>
                    <h1 class="font-bold text-[48px] font-bold text-center">What I am capable of?</h1>
                    <div class="flex flex-wrap justify-center items-center gap-6">
                        <div  v-for="el in data1.data._rawValue" :key="el.id" class="flex justify-center items-center gap-10 mt-10">
                            <img :src="el.skill_icon" alt="HTML" class="w-[150px] h-[120px]">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section id="project" class="py-10">
        <div class="container mx-auto ">
            <div class="grid jusrify-beetwen items-center ">
                <p class="font-bold text-[24px] text-blue-500 font-bold text-center">Projects</p>
                <h1 class="font-bold text-[48px] font-bold text-center">What I have made?</h1>
                    <div class="project_s flex flex-wrap justify-center items-center gap-10 mt-10">
                       <div v-for="el in data.data._rawValue" :key="el.id" class="cards w-[30%] h-full border card grid justify-beetwen shadow-lg shadow-gray-600 ">
                            <img :src="el.project_img" alt="" class="projectimg w-full h-[300px]">
                            <div class="projecttext px-5 py-5 grid gap-3 border-4 border-t-gray-500  ">
                                <h1 class="font-bold text-[24px]">{{el.project_name}}</h1>
                                <p class="text-[18px] h-[60px]">{{el.description}}</p>
                                <div class="w-full text-blue-600 flex items-center justify-beetwen gap-6">
                                    <a :href="el.project_link">Project Link</a>
                                    <a :href="el.link_github_project">Github Link</a>
                                </div>
                            </div>
                       </div>
               <!-- ================================ -->
                </div>
            </div>
        </div>
    </section>
    <Footer/>
</template>

<script setup>
    // const data = await useFetch('http://localhost:1987/api/project')
    const data = await useFetch('https://masterusmanov.onrender.com/api/project')
    // const data1 = await useFetch('http://localhost:1987/api/skills')
    const data1 = await useFetch('https://masterusmanov.onrender.com/api/skills')
</script>

<style lang="scss" >
    *{
        scroll-behavior: smooth;
    }
    @media only screen and (max-width: 1024px) {
        .mypic{
            width: 300px;
            margin-left: 50px;
        }
        .projectimg{
            height: 170px;
        }
        .projecttext h1{
            font-size: 14px;
        }
        .projecttext p{
            font-size: 12px;
        }
        .projecttext a{
            font-size: 14px;
        }
    }
    @media only screen and (max-width: 876px) {
        .hi h1{
            font-size: 24px;
        }
        .mypic{
            width: 250px;
            margin-left: 50px;
        }
        .projectimg{
            height: 170px;
        }
        .projecttext h1{
            font-size: 14px;
        }
        .projecttext p{
            font-size: 12px;
        }
        .projecttext a{
            font-size: 14px;
        }
    }
    @media only screen and (max-width: 668px) {
        .hi{
            display: grid;
            padding-left: -50px;
         }
        .hi h1{
           font-size: 18px;
        }
        .hi p{
            font-size: 14px;
        }
        .hi a{
            display: none;
        }
        .myypic{
            width: 100%;
        }
        .mypic{
            width: 250px;
            justify-items: center;
          
        }
        .about1{
            width: 100%;
            padding: 10px;
        }
        .about1 h1{
            
            text-align: center;
        }
        .text p{
            font-size: 14px;
        }
        .project_s{
            display: grid;
        }
        .cards{
            width: 100%;
        }
        .projectimg{
            width: 100%;
            height: 250px;
        }
        .projecttext h1{
            font-size: 20px;
        }
        .projecttext p{
            font-size: 16px;
        }
        .projecttext a{
            font-size: 14px;
        }
        .abpic{
            display: none;
        }
        .haq{
            text-align: center;
        }
        .about{
            width: 100%;
            text-align: center;
            padding-left: 10px;
        }
       
    }
</style>
