<template>
    <div class="hero-body cv-body ">
        <div class="container">
            <div class="columns  is-multiline  is-centered">
                <div class="column is-full is-hidden-tablet mobile-resume-info is-multiline">
                    <p>Rudy Quevedo |
                        <a href='mailto:rudy@iamsmarts.com'>rudy@iamsmarts.com</a> |
                        <a href="#">213.880.9304</a></p>
                </div>
                <div class="column is-3 is-offset-9 is-hidden-touch">
                    <p>Rudy Quevedo</p>
                    <p>445 Sout Ardmore Avenue,</p><p>Los Angeles, CA 90020</p>
                    <p><a href='mailto:rudy@iamsmarts.com'>rudy@iamsmarts.com</a></p>
                    <p><a href="#">213.880.9304</a></p>
                </div>
                <div class="column is-full is-mobile">
                    <h1 class="experience-title">Experience</h1>
                    <div  v-for="(job, index) in rData" :key="index" class="column is-8 experience-body is-multiline">
                        <div class="experience-copy">
                            <h2>{{job.company}}</h2>
                            <p class="date"><em>{{job.dates}}</em></p>
                            <ul>
                                <li v-for="(responsibility, index) in job.responsibilities" :key="index">
                                    {{responsibility}}
                                </li>
                            </ul>
                            <p class="tools-desc"><strong>{{job.toolsDescription}}</strong></p>
                            <p>{{job.toolsList}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import resumeData from '@/data/resume-data';
// import Hero from '@/components/Hero.vue'
export default {
    name:'Resume',
    data: () => ({
        rData: resumeData,
    }),
}
</script>
<style lang="scss" scoped>
.cv-body{
    .experience-title{
        border-bottom:.2rem solid gray;
    }
}
.mobile-resume-info{
    a{
        color: red;
        background:none;
    }
}
.personal-info{
    width: 100%;
}
.experience-body{
    margin: 1.5rem 0;
    font-size: 1.6rem;
    border-bottom: solid 1px gray;
    padding-bottom: 25px;
    .experience-copy{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        h2, .copy{
            font-size: 2rem;
            font-weight: bold;
            width: 50%;
        }
        .date{
            text-align: right;
            font-size: 1.8rem;
            line-height: 1.5;
        }
        .responsibility{
            margin-top: 1.5rem;
        }
        ul{
            margin: 1rem 0;
            width: 100%;
            li{
                margin: 0 0 0.5rem 0;
                text-indent: -5px;
                &:before{
                    content: "-";
                    text-indent: -5px;
                }
            }
        }
        .tools-desc{
            width: 100%;
        }
    }
}
</style>
