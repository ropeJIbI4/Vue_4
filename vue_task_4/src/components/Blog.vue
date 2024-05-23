<template>
    <div class="header center">
        <div class="header__nav">
            <div>
                <img class="header__logo" src="/public/assets/Logo_header.png" alt="">
            </div>
            <div class="header__link">
                <a href="#">Home</a>
                <a href="#">Project</a>
                <a href="#">Blog</a>
            </div>
        </div>
        <div class="header__content center">
            <div class="header__content__top">
                <h1 class="header__content__top__title">Articles & News</h1>
                <p class="header__content__top__parag">Home / Blog</p>
            </div>
        </div>
    </div>
    <div class="top__content center">
        <h1 class="top__content__title">Latest Post</h1>
        <div class="top__content__content">
            <div class="top__content__img">

            </div>
            <div class="top__content__info">
                <h2 class="top__content__info__title">Low Cost Latest Invented Interior Designing Ideas</h2><br><br>
                <p class="top__content__info__parag">Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis
                    dignissim maximus.posuere in.Contrary to popular
                    belief.</p><br><br>
                <p class="top__content__info__parag">Lorem Ipsum is not simply random text. It has roots in a piece of
                    classica.</p>
                <div class="top__content__info__link">
                    <p class="top__content__info__link__parag">26 December,2022</p>
                    <a href="#"><button class="top__content__info__link__btn"><img src="/public/assets/btn_3.png"
                                alt=""></button></a>
                </div>
            </div>
        </div>
    </div>
    <div>
        <h2 class="article__title">Articles & News</h2>
        <div class="article__news">
            <div class="article__news__item" v-for="(item, index) in articleNewsData" :key="index">
                <img class="article__news__image" :src="item.image" :alt="item.title">
                <h2 class="article__news__text">{{ item.title }}</h2>
                <div class="article__news__info">
                    <p class="article__news__info__parag">26 December,2022</p>
                    <a href="#"><button class="article__news__info__btn"><img src="/public/assets/btn_3.png"
                                alt=""></button></a>
                </div>
            </div>
            <div class="article__news__link"><a href="#"><img src="/public/assets/1.png" alt=""></a><a href="#"><img
                        src="/public/assets/2.png" alt=""></a><a href="#"><img src="/public/assets/3.png" alt=""></a><a
                    href="#"><img src="/public/assets/4.png" alt=""></a></div>
        </div>
    </div>
    <div class="footer">
        <div class="footer__1">
            <div>
                <img class="footer__logo__1" src="/public/assets/Logo_header.png" alt="">
                <p class="footer__parag">It is a long established fact that a reader will be distracted lookings.</p>
                <div class="footer__logo__2">
                    <a href="#"><img src="/public/assets/twit.png" alt=""></a>
                    <a href="#"><img src="/public/assets/in.png" alt=""></a>
                </div>
            </div>
        </div>
        <div class="footer__2">
            <h3>Pages</h3><br>
            <ul>
                <li><a href="#">Home</a></li><br>
                <li><a href="#">Project</a></li><br>
                <li><a href="#">Blog</a></li><br>
            </ul>

        </div>
        <div class="footer__3">
            <h3>Contact</h3><br>
            <p>55 East Birchwood Ave.</p><br>
            <p>New York, NY 10001</p><br>
            <p>contact@interno.com</p> <br>
            <p>(123) 456 - 7890</p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            articleNewsData: [
                {
                    image: '/public/assets/article_1.png',
                    title: 'Let’s Get Solution For Building Construction Work',
                },
                {
                    image: '/public/assets/article_2.png',
                    title: 'Low Cost Latest Invented Interior DesigningIdeas',
                },
                {
                    image: '/public/assets/article_3.png',
                    title: 'Best For Any Office & Business Interior Solution',
                },
                {
                    image: '/public/assets/article_4.png',
                    title: 'Let’s Get Solution For Building Construction Work',
                },
                {
                    image: '/public/assets/article_5.png',
                    title: 'Low Cost Latest Invented Interior Designing Ideas.',
                },
                {
                    image: '/public/assets/article_6.png',
                    title: 'Best For Any Office & Business Interior Solution',
                }
            ],
        };
    },
};
</script>



<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;

}

a {
    text-decoration: none;
    color: black;
}

.center {
    padding-left: calc(50% - 560px);
    padding-right: calc(50% - 560px);
}

.header__nav {
    padding-right: 10px;
    padding-left: 10px;
    display: flex;
    justify-content: space-between;
}

.header__link {
    display: flex;
    padding-top: 15px;
    gap: 15px;
}

.header__logo {
    width: 176px;
}

.header__content {
    display: flex;
    justify-content: center;
    text-align: center;
    align-items: flex-end;
    background-image: url(/public/assets/back_2.png);
    background-size: cover;
    background-position: center;
    height: 356px;
}

.header__content__top__title {
    font-size: 38px;
    font-family: "DM Serif Display", serif;
    font-weight: 400;
    font-style: normal;
    text-align: left;
    padding-left: 30px;
}

.header__content__top__parag {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-size: 22px;
    font-style: normal;
    white-space: normal;
}

.header__content__top {
    padding: 41px 78px;
    width: 503px;
    border: solid 1px;
    border-radius: 30px 30px 0px 0px;
    border-color: #FFFFFF;
    background-color: #FFFFFF;

}

.top__content {
    margin-top: 120px;
    width: 1200px;


}

.top__content__title {
    font-size: 50px;
    font-family: "DM Serif Display", serif;
    font-weight: 400;
    font-style: normal;
    text-align: left;
    padding-left: 30px;
}


.top__content__content {
    padding-top: 25px;
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: center;
    align-items: center;
}

.top__content__img {
    border-radius: 40px;
    width: 569px;
    height: 478px;
    background-image: url(/public/assets/top_content.png);
}

.top__content__info {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding-left: 20px;
    width: 489px;
}

.top__content__info__title {
    font-size: 30px;
    font-family: "DM Serif Display", serif;
    font-weight: 400;
    font-style: normal;
    white-space: pre-line
}

.top__content__info__parag {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-size: 22px;
    font-style: normal;
    white-space: normal;
}

.top__content__info__link {
    display: flex;
    align-items: flex-end;
    flex-direction: row;
    gap: 270px;
    padding-top: 35px
}

.top__content__info__link__parag {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-size: 16px;
    font-style: normal;
    white-space: normal;
}

.top__content__info__link__btn {
    border: none;
    background-color: white;
}

#app {
    margin-top: 100px;
    padding-left: 52px;
}

.article__title {
    font-size: 50px;
    font-family: "DM Serif Display", serif;
    font-weight: 400;
    font-style: normal;
    white-space: pre-line;
    text-align: left;
}

.article__news {
    margin-top: 25px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 3px;



}

.article__news__item {
    text-align: center;
    border: solid 1px whitesmoke;
    border-radius: 40px;
    width: 382px;

}

.article__news__text {
    font-size: 25px;
    font-family: "DM Serif Display", serif;
    font-weight: 400;
    font-style: normal;
    white-space: pre-line;
    text-align: left;
}

.article__news__info {
    display: flex;
    align-items: flex-end;
    flex-direction: row;
    gap: 150px;
    padding-top: 35px;
}

.article__news__info__parag {
    font-family: "Jost", sans-serif;
    font-weight: 400;
    font-optical-sizing: auto;
    font-style: normal;
    font-size: 16px;
    white-space: normal;
    padding-left: 25px;
    padding-bottom: 20px;
}

.article__news__info__btn {
    border: none;
    background-color: white;
}

.article__news__link {
    display: flex;
    gap: 15px;
    margin-top: 15px;
}

.footer {
    margin-top: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding-left: 65px;
}

.footer__parag {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
    padding-top: 10px;
    padding-bottom: 10px;

}

.footer__1 {
    width: 390px;
}

.footer__1 p {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
    width: 290px;
}

.footer__2 {
    width: 390px;
    text-align: center
}

.footer__3 {
    width: 390px;
    text-align: center
}

.footer__3 h3 {
    font-family: "DM Serif Display", serif;
    font-weight: 400;
    font-style: normal;
}

.footer__3 p {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
}

.footer__logo__1 {
    width: 120px;
}

.footer__logo__2 {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    gap: 15px;
}

ul {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
    list-style: none;
}
</style>