<template>
    <section class="feedback container">
        <div class="feedback__body">
            <div class="form__main">
                <div class="form__title">
                    <h2>Заполните форму для <span>связи с нами.</span></h2>
                </div>
                <form action="" method="post">
                <label for="name">
                    <input placeholder="Имя" type="text" name="firstName" id="firstName">
                </label>
                <label for="surname">
                    <input placeholder="Фамилия" type="text" name="surName" id="surName">
                </label>
                <label for="email">
                    <input placeholder="E-mail" type="email" name="email" id="email">
                </label>
                <textarea name="message" id="message" cols="45" rows="1" placeholder="Сообщение"></textarea>
                
                <button class="form__button">
                    <span>Отправить сообщение</span>
                </button>
                </form>
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
        margin: 60px 44px;
        border: 9px solid #6ca09f;
        border-radius: 36px;
    }
    .form__background {
        background:  url('../assets/background/shest.svg') 110px -330px no-repeat;
        width: 429px;
        height: 327px;
    }
    .form__main {
        max-width: 440px;
        padding: 16px;
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
    input {
        margin: 10px 0 10px 0;
        border: none;
        border-bottom: 1px solid #6b6b6b;
        background-color: transparent;
        outline: none;
    }
    input#surName {
        margin-left: 20px;
    }
    textarea {
        resize: none;
        margin: 10px 0 10px 0;
        border: none;
        border-bottom: 1px solid #6b6b6b;
        background-color: transparent;
        outline: none;
    }
    /* #firstName {
        border: none;
        border-bottom: 1px solid #6b6b6b;
        background-color: transparent;
        outline: none;

    } */
    .form__button {
        padding: 10px;
        margin-top: 32px;
        cursor: pointer;
        box-shadow:  4px 4px 8px 0px rgba(34, 60, 80, 0.2);
        text-align: center;
        font-size: 16px;
        padding: 5px;
        color: #fff;
        font-weight: 400;
        max-width: 260px;
        height: auto;
        background-color: #6ca09f;
        border: solid 2px #5a7fb7;
        border-radius: 4px;
        transition: all ease .5s;
        &:hover {
            transform: scale(110%);
            //transform: rotate(360deg);
        }
    }
</style>