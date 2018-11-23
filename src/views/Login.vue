<template>
    <div class="box">
        <div class="logBox">
            <div class="line">
                <input placeholder="e-mail" type="text" class="line-user"/>
            </div>
            <div class="line line-pwd">
                <input placeholder="密 码" type="password" class="line-pwd"/>
            </div>
            <div class="check">
                <ul>
                    <li v-on:click="forget">
                        <van-checkbox v-model="checked" checked-color="#2DCB70">忘记密码</van-checkbox>
                    </li>
                </ul>

            </div>
            <div class="btn">
                <van-button round type="danger">登 录</van-button>
            </div>
            <div class="setin">
                <van-button round type="danger">注 册</van-button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Login",
        data() {
            return {
                checked: ''
            };
        },
        methods: {
            forget: function () {
                return alert('密码修改成功！')
            }
        }
    }
</script>

<style scoped lang="scss">
    .box {
        background: url("../../public/img/login/bg-2.png") no-repeat;
        position: fixed;
        width: 100%;
        height: 100%;
    }

    .logBox {
        position: relative;
        top: 27.5rem;
        left: 4rem;
    }

    .logBox .line {
        margin-bottom: 0.5rem;
        padding: 1rem;
    }

    .line input {
        width: 70%;
        height: 3rem;
        border-top: 0;
        border-left: 0;
        border-right: 0;
        border-bottom: 0.1rem solid #DCDFE6;
        padding: 0.5rem 0 0 4rem;
        outline: none;
        font-family: 微软雅黑;
        transition: border-bottom-color ease 200ms;
        font-size: 1.5rem;
    }

    input:hover {
        border-bottom: 0.1rem solid #606266;
    }

    .line .line-user {
        background: url("../../public/img/icons/msg-1.png") no-repeat;
        background-position: 1px;
    }

    .line .line-pwd {
        background: url("../../public/img/icons/earth-1.png") no-repeat;
        background-position: 1px;
    }

    .line .line-user:hover {
        background: url("../../public/img/icons/msg-2.png") no-repeat;
        background-position: 1px;
    }

    .line .line-pwd:hover {
        background: url("../../public/img/icons/earth-2.png") no-repeat;
        background-position: 1px;
    }

    .check {
        padding-left: 1rem;
        margin: 0 auto;
    }

    .box .btn {
        margin-top: 1rem;
        margin-left: 0.8rem;
    }

    .btn button {
        display: inline-block;
        width: 80%;
        text-decoration: none;
        height: 3.5rem;
        line-height: 3.5rem;
        color: white;
        background: green;
        border: 0;
        opacity: 0.7;

    }

    .setin {
        margin-top: 1rem;
        margin-left: 0.8rem;
    }
    .setin button{
        display: inline-block;
        width: 80%;
        text-decoration: none;
        height: 3.5rem;
        line-height: 3.5rem;
        color: white;
        background: #FFD700;
        border: 0;
        opacity: 1;
    }
</style>