<template>
    <section class="feedback container">
        <div class="feedback__body">
            <div class="form__main">
                <div class="form__title">
                    <h2>Заполните форму для <span>связи с нами.</span></h2>
                    <div class="form__button">
                        <span>Отправить сообщение</span>
                    </div>
                </div>
            </div>
            <div class="form__background"></div>
        </div>
    </section>
</template>

<script>
    export default {
      name: 'FeedbackForm'     
    }
</script>

<style scoped lang="scss">
    .feedback__body {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        max-width: 100%;
        height: auto;
        margin: 60px 62px;
        border: 9px solid #6ca09f;
        border-radius: 36px;
    }
    .form__background {
        background:  url('../assets/background/form__background.svg') top right no-repeat;
        width: 429px;
        height: 327px;
    }
    .form__main {
        max-width: 340px;
        height: auto;
        margin: 96px auto;
        h2 {
            font-size: 36px;
            font-weight: 500;
            color: #6b6b6b;
            span {
                color: #6ca09f;
                font-weight: 500;
            }
        }
    }
</style>