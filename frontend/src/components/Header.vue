<template>
    <div class="header featurebox col-md-12 col-sm-12 col-xs-12">
        <div class="row" align="center">

            <div class="name col-md-10 col-sm-10 col-xs-10">
                <p class="mainText">{{ msg }}</p>
            </div>

            <div class="loginBlock col-md-2 col-sm-2 col-xs-2">
                <form method="POST" action="/login">
                    <button type="submit" class="login">
                        Login
                        <!--<img src="../assets/img/login.jpg" alt="Login"/>-->
                    </button>
                </form>

                <form :action="msg3">
                    <button type="submit">
                        {{ msg2 }}
                    </button>
                </form>

                <!--<p class="greeting">{{#greeting}} {{.}} {{/greeting}}</p>-->
            </div>
        </div>
    </div>
</template>

<style>
    .header{
        height: 100px;
        border: 1px solid black;
    }

    .name{
        margin: 32px auto;
        text-align: center;
    }

    .loginBlock img{
        width: 100%;
    }

    .loginBlock button{
        /*background: black;*/
        background: linear-gradient(180deg, grey, black);
        width: 120px;
        height: 45px;
        border-radius: 8px;
        margin-top: 2px;
        font-size: 14px;
        color: white;
    }

    .mainText{
        font-size: 23px;
    }
</style>

<script>
    export default {
        props: ['msg', 'msg2', 'msg3'],
        data(){
            return{}
        }
    }
</script>