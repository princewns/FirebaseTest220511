<template>
<div>
    <h1>메인 페이지 입니다.</h1>
    <img v-if="fnGetUser.photoURL" :src="fnGetUser.photoURL">
    <h3>{{fnGetUser.name}}</h3>
    <p>{{fnGetUser.email}}</p>
</div>
</template>

<script>
export default {
    computed : {
        fnGetUser() {
            let userInfo = this.$store.getters.fnGetUser;
            return userInfo;
        }
    }
}
</script>