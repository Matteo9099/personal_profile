<template>
    <div class="skills-template vh-100">
        <div class="pt-5" data-aos="fade-up">
            <h1 class="text-center text-white ms_skills">SKILLS</h1>
        </div>
        
        <section class="container d-flex m-auto justify-content-center row pb-5">

            <div class="mt-5 col-md-4 d-flex justify-content-center" data-aos="fade-up">
                <div class="card ms_bg_front" style="width: 18rem;" v-for="(front, index) in fronts" :key="index">
                    <div class="d-flex justify-content-center">
                        <h3 class="text-white">{{ front.title }}</h3>
                    </div>
                    <hr style="margin:0;">
                    <div class="card-body">
                        <ul class="list-group list-group-flush text-center"> 
                            <li class="list-group-item" v-for="(skill,index) in front.skills" :key="index">
                                {{ skill }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="mt-5 col-md-4 d-flex justify-content-center" data-aos="fade-up">
                <div class="card ms_bg_back" style="width: 18rem;" v-for="(back, index) in backs" :key="index">
                    <div class="d-flex justify-content-center">
                        <h3 class="text-white">{{ back.title }}</h3>
                    </div>
                    <hr>
                    <div class="card-body">
                        <ul class="list-group list-group-flush text-center"> 
                            <li class="list-group-item" v-for="(skill,index) in back.skills" :key="index">
                                {{ skill }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="mt-5 col-md-4 d-flex justify-content-center" data-aos="fade-up">
                <div class="card ms_bg_fram" style="width: 18rem;" v-for="(framework, index) in frameworks" :key="index">
                    <div class="d-flex justify-content-center">
                        <h3 class="text-white">{{ framework.title }}</h3>
                    </div>
                    <hr>
                    <div class="card-body">
                        <ul class="list-group list-group-flush text-center"> 
                            <li class="list-group-item" v-for="(skill,index) in framework.skills" :key="index">
                                {{ skill }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>

        </section>

        <div class='light x1'></div>
        <div class='light x2'></div>
        <div class='light x3'></div>
        <div class='light x4'></div>
        <div class='light x5'></div>
        <div class='light x6'></div>
        <div class='light x7'></div>
        <div class='light x8'></div>
        <div class='light x9'></div>
    </div>
</template>

<script>


export default {
    name: "SkillsView",
    data() {
        return {
            fronts: [
                {
                    title: "Front-End",
                    skills: [
                        "HTML5",
                        "CSS",
                        "JAVASCRIPT",
                        "SASS",
                    ]
                }
            ],
            backs: [
                {
                    title: "Back-End",
                    skills: [
                        "PHP",
                        "JAVA"
                    ]
                }
            ],
            frameworks: [
                {
                    title: "Framework & Tools",
                    skills: [
                        "BOOTSTRAP",
                        "VUE.JS",
                        "NODE.JS",
                        "LARAVEL",
                        "PhpMyAdmin",
                        "MYSQL",
                        "GIT",
                        "GITHUB",
                        "FIGMA",
                        "CANVA"
                    ]
                }
            ]
        };
    },
 
}
</script>

<style scoped lang="scss">

.ms_bg_front{
    background: url('../assets/img/eagle.png') no-repeat;
    background-position: center;
    background-size: cover;
}
.ms_bg_back{
    background: url('../assets/img/elephant.png') no-repeat;
    background-position: center;
    background-size: cover;
}
.ms_bg_fram{
    background: url('../assets/img/lion.png') no-repeat;
    background-position: center;
    background-size: cover;
}

li{
    background-color: transparent;
    color: #fff;
    font-weight: bold;

    &:hover{
        border: 1px solid gray;
        transform: scale(1.1);
        background-color: rgb(158, 157, 157);
    }
 }


</style>