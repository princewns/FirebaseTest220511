<template>
<div>
    <h1>시작페이지</h1>
    <a @click="fnDoGoogleLoginPopup">구글 로그인</a><br>
    <a href="/login">이메일 로그인</a>
</div>
</template>

<script>
export default {
    methods : {
        fnDoGoogleLoginPopup() {
            this.$store.dispatch("fnDoGoogleLoginPopup");
        }
    }
}
</script>