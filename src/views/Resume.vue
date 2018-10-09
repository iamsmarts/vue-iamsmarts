<template>
    <div class="hero-body cv-body ">
        <div class="container columns  is-multiline  is-centered">
            <div class="column is-3 is-offset-9">
                <p>Rudy Quevedo</p>
                <p>445 Sout Ardmore Avenue,</p><p>Los Angeles, CA 90020</p>
                <p><a href='mailto:rudy@iamsmarts.com'>rudy@iamsmarts.com</a></p>
                <p><a href="#">213.880.9304</a></p>
            </div>
            <div class="column is-full is-mobile">
                <h1 class="experience-title">Experience</h1>
                <div class="column is-8 experience-body is-multiline">
                    <div class="experience-copy">
                        <h2>hi5.agency</h2>
                        <p class="date"><em>5/17 - present</em></p>
                        <p class="responsibility"><strong>Responsibilities:</strong></p>
                        <ul>
                            <li> Serve as clients point of contact for tech projects</li>
                            <li> Determine level of effort for tech projects for finance teams.</li>
                            <li> Interview and write code test for freelance and full time candidates.</li>
                            <li> Collaborate with design team to ensure design needs are met</li>
                            <li> Identify best fit libraries / frameworks for both present and prototype projects.</li>
                            <li> Architect and scaffold projects start off point. </li>
                            <li> Hands on development of projects from comps to deployment</li>
                            <li>Mentoring and coaching of Jr developers to uphold a high standard of code quality. </li >
                        </ul>
                        <p><strong>Tools I've been using:</strong></p>
                        <p>VueJS, Vuex, ReactJS, AWS Lambda, AWS API Gateway, AWS DynamoDB, ecmascript 6, CSS grid, CSS3, HTML5, Sass, Git, NPM, Webpack, bootstrap, foundation, along with other tools.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'Resume'
}
</script>
<style lang="scss" scoped>
.cv-body{
    .experience-title{
        border-bottom:.2rem solid gray;
    }
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
            li{
                margin: 0 0 0.5rem 0;
                text-indent: -5px;
                &:before{
                    content: "-";
                    text-indent: -5px;
                }
            }
        }
    }
}
</style>
