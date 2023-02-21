<template>
    <div class="title">
        <h1 class="title_text">
            <slot name="title"></slot>
        </h1>
        <h3 class="subtitle">
            <slot name="subtitle"></slot>
        </h3>
        <MyButton>VIEW PROJECT</MyButton>
    </div>
</template>

<script>
import MyButton from './MyButton.vue';

    export default {
    components: { MyButton }
}
</script>

<style scoped>
.title {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.title_text {
    text-align: center;
    font-size: 150px;
    line-height: 150px;
    font-weight: 400;
    color: #FFF;
    margin-bottom: 30px;
}
.subtitle {
    font-size: 24px;
    line-height: 38px;
    font-weight: 400;
    color: #FFF;
    margin-bottom: 100px;
}
@media screen and (max-width: 570px) {
    .title_text {
        font-size: 60px;
        line-height: 90px;
        margin-bottom: 10px;
    }
    .subtitle {
        margin-bottom: 40px;
        font-size: 20px;
        line-height: 34px;
    }
}
@media screen and (min-width:570px) and (max-width: 900px) {
    .title_text {
        font-size: 120px;
        line-height: 150px;
        margin-bottom: 15px;
    }
    .subtitle {
        margin-bottom: 50px;
        font-size: 20px;
        line-height: 34px;
    }
}
</style>