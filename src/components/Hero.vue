<template>
    <div class="hero">
        <div class="info">
            <div class="title">
                <!-- <h1>
                    <span>front end dev</span><br>
                    Rudy Quevedo
                </h1> -->
                <h1>
                    <span>some not tot</span><br>
                    some quezals
                </h1>
            </div>
            <div class="nav">
                <nav>
                    <ul>
                        <li><a href="#">home</a></li>
                        <li><a href="#">about</a></li>
                        <li><a href="#">contact</a></li>
                    </ul>
                </nav>
                <div class="updated">
                    <p class="last-update-title">LAST UPDATED:</p>
                    <p class="last-update-date">9.7.18</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Hero',
}
</script>

<style scoped lang="scss">
$break-small: 380px;
$break-large: 1020px;

.hero{
    width: 100%;
    min-height: 75px;
    background-color: #000;
    background-image: url('../assets/dark.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    .info{
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        justify-content: flex-start;
        align-content: flex-start;
        align-items: flex-end;
        height: 100%;
        min-height: 200px;
        width: 100%;
        margin: 5px;
        .title{
            order: 0;
            flex: 2 1 auto;
            align-self: auto;
            width: 100%;
            display: flex;
            flex-direction: column;
            align-content: flex-end;
            justify-content: flex-end;
            h1{
                color: #fff;
                text-transform: uppercase;
                font-size:18px;
                line-height: 14px;
                letter-spacing: -1px;
                margin: 0px;
                text-align: right;
                span{
                    font-size:14px;
                }
            }
        }
        .nav{
            order: 0;
            flex: 1 0 auto;
            align-self: auto;
            width: 100%;
            display: flex;
            flex-direction: column;

            nav{
                ul{
                    list-style: none;
                    display: flex;
                    flex-direction: row;
                    flex-wrap: wrap;
                    text-align: right;
                    justify-content: flex-end;
                    padding: 0px;
                    margin: 5px 0px;
                    li{
                        margin-left: 15px;
                        a{
                            color: #fff;
                            text-decoration: none;
                            text-transform: uppercase;
                            font-size:18px;
                            line-height: 14px;
                            letter-spacing: -1px;
                            &:hover{
                                background: #fff;
                                color: #000;
                                padding: 0px 5px;
                                transition: all 0.25s ease;
                            }
                        }
                    }
                }
            }
            .updated{
                display: flex;
                flex-direction: column;
                align-content: flex-end;
                justify-content: flex-end;
                p{
                    margin: 0px;
                    font-size: 14px;
                    text-align: right;
                    color: #fff;
                }
            }
        }
    }
    @media screen and (min-width: $break-large) {
        min-height: 320px;
        justify-content: flex-end;
        .info{
            min-height: 304px;
            width: 20%;
            min-width: 250px;
            display: flex;
            flex-direction: column;
            flex-wrap: nowrap;
            justify-content: flex-end;
            align-content: stretch;
            align-items: flex-end;
        }
    }
}
</style>

