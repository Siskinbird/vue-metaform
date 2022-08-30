<template>
    <section class="feedback">
        <div class="container">
        <div class="feedback__body container" data-aos="zoom-in" data-aos-duration="1000">
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
                    <input required placeholder="E-mail" type="email" name="email" id="email">
                </label>
                <textarea required name="message" id="message" cols="45" rows="1" placeholder="Сообщение"></textarea>
                
                <button type="submit" class="form__button">
                    <span>Отправить сообщение</span>
                </button>
                </form>
            </div>
            <div class="form__background"></div>
        </div>
    </div>
    </section>
</template>

<script>
    export default {
      name: 'FeedbackForm'     
    }
</script>

<style scoped lang="scss">
    @mixin tablet-portrait {
        @media (max-width: 600px) { @content; }
    }
    @mixin tablet-small {
        @media (max-width: 500px) { @content; }
    }
    .container {
        padding: 0;
    }

    .feedback {
        margin-top: 60px;
        background: url('../assets/background/bgpattern2.png') repeat;
        padding: 10px;
    }

    .feedback__body {
        background:  url('../assets/background/shesternya.svg') -67px -66px no-repeat;
        background-color: #fff;
        box-shadow: 8px 8px 10px 0px rgba(34, 60, 80, 0.2);
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        max-width: 100%;
        height: auto;
        margin: 60px 44px;
        border: 9px solid #6ca09f;
        border-radius: 36px;
        @include tablet-small {
            margin: 0;
             border: 4px solid #6ca09f;
        }
    }

    .form__background {
        background:  url('../assets/background/form__background.svg') -1px -5px no-repeat;
        width: 429px;
        height: 327px;
        @include tablet-small {
            display: none;
        }     
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
            @include tablet-portrait {
                font-size: 28px;
                text-align: center;
            }
        }
            @include tablet-small {
            margin: 22px auto;
        }
    }

    form {
        margin-top: 60px;
        @include tablet-small {
            display: flex;
            flex-direction: column;
        }
    }

    input {
        margin: 10px 0 10px 0;
        border: none;
        border-bottom: 1px solid #6b6b6b;
        background-color: transparent;
        outline: none;
    }

    input#firstName {
        @include tablet-small {
            width: 260px;
        }
    }

    input#surName {
        margin-left: 20px;
            @include tablet-small {
                margin-left: 0;
                width: 260px;
            }
    }

    textarea {
        resize: vertical;
        margin: 20px 0 10px 0;
        padding-bottom: 12px;
        border: none;
        border-bottom: 1px solid #6b6b6b;
        background-color: transparent;
        outline: none;
        @include tablet-small {
            width: 260px;
        }
    }

    input[type=text] {
    padding: 12px 0;
    margin: 8px 0;
    box-sizing: border-box;
    }

    input[type=email] {

    padding: 12px 0;
    margin: 8px 0;
    box-sizing: border-box;
    }
    #email {
        width: 338px;
        @include tablet-small {
            width: 260px;
        }
    }
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