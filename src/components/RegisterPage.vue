<template>
<div>
    <h1>회원가입 페이지 입니다.</h1>
    <form @submit.prevent="fnRegisterUser">
        <label for="">이메일</label>
        <input type="text" v-model="email"><br>
        <label for="">비밀번호</label>
        <input type="password" v-model="password"><br>
        <input type="submit" value="로그인">
    </form>
</div>
</template>

<script>
export default {
    data() {
        return{
            email : '',
            password : ''
        }
    },
    methods : {
        fnRegisterUser() {
            this.$store.dispatch("fnRegisterUser", {
                pEmail : this.email,
                pPassword : this.password
            });
        }
    }
}
</script>