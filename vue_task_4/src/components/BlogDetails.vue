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
    </div>
    <div class="content__block center"></div>
    <div class="center">
        <div class="blog_news">
            <div class="tags">
                <div>
                    <h2 class="blog_news__title">Tags</h2>
                </div>
                <div>
                    <button class="tag" v-for="(tag, index) in tags" :key="index" @click="selectTag(tag)"
                        :class="{ active: selectedTag === tag }">
                        {{ tag }}
                    </button>
                </div>
            </div>
            <div class="blog_news__items">
                <div class="blog_news__item" v-for="(item, index) in filteredBlog" :key="index">
                    <h2 class="blog_news__title">{{ item.title_1 }}</h2>
                    <img class="blog_news__image__1" :src="item.image_1" :alt="item.image_is_none">
                    <div v-if="item.text_1 != ''" class="blog_news__block">
                        <p class="blog_news__text">26 December,2022</p>
                        <p class="blog_news__text">Interior / Home / Decore</p>
                    </div>
                    <p class="blog_news__text">{{ item.text_1 }}</p>
                    <br>
                    <p class="blog_news__text">{{ item.text_2 }}</p>
                    <br>
                    <div v-if="item.text_1 != ''" class="blog_news__reconstruct">
                        <img class="blog_news__image__2" :src="item.image_is_none" :alt="item.text_image_is_none">
                        <p class="blog_news__text__reconstruct">{{ item.text_image_is_none }}</p>
                    </div>
                    <h2 class="blog_news__title">{{ item.title_2 }}</h2>
                    <br>
                    <p class="blog_news__text">{{ item.text_3 }}</p>
                    <br>
                    <ol TYPE=1 v-if="item.text_1 != ''">
                        <li>1 {{ item.text_li_1 }}</li><br>
                        <li>2 {{ item.text_li_1 }}</li><br>
                        <li>3 {{ item.text_li_1 }}</li><br>
                    </ol>
                    <div>
                        <img class="blog_news__image__3" :src="item.image_1" :alt="item.image_is_none">
                        <p class="blog_news__text">{{ item.text_4 }}</p>
                    </div>
                </div>
            </div>
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
            selectedTag: null,
            blogNewsData: [
                {
                    image_1: "/public/assets/content_1_dz_3.png",
                    image_2: "/public/assets/content_2_dz_3.png",
                    image_is_none: "/public/assets/image_is_none.png",
                    title_1: "Let’s Get Solution for Building Construction Work",
                    title_2: "Design sprints are great",
                    text_1:
                        "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable.",
                    text_2:
                        "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
                    text_3:
                        "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
                    text_4:
                        "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
                    text_li_1:
                        "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
                    text_image_is_none: "The details are not the details. They make the design.",
                    tags: ["Kitchen",],
                },
                {
                    image_1: "",
                    title_1: "",
                    text_1: "",
                    tags: ["Bedroom", "Building", "Architecture", "Kitchen Planning", "Bedroom"],
                },
            ],
        };
    },
    computed: {
        tags() {
            return Array.from(new Set(this.blogNewsData.map((blog) => blog.tags).flat()));
        },
        filteredBlog() {
            if (!this.selectedTag) {
                return this.blogNewsData;
            }

            return this.blogNewsData.filter((blog) => blog.tags.includes(this.selectedTag));
        },
    },
    methods: {
        selectTag(tag) {
            this.selectedTag = tag;
        },
    },
};
</script>

<style>
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

.content__block {
    background-image: url(/public/assets//Image_laceholder.png);
    height: 351px;
    background-size: cover;
    background-position: center;
    margin-bottom: 100px;
}

.tags {
    display: flex;
    height: 100px;
    width: 930px;
    padding-top: 100px;
    align-content: stretch;
    justify-content: center;
    flex-direction: column;
}


.tag {
    width: 40%;
    height: 30px;
    line-height: 15px;
    text-align: center;
    border: 1px solid black;
    box-sizing: border-box;
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;

}

.tag:active::after {
    background-color: black;
}

.tag {
    border: solid 1px #F4F0EC;
    border-color: #F4F0EC;
    border-radius: 40px;
}


.tag.active {
    background-color: #292F36;
    color: white;
}

.tag:hover {
    background-color: red;
}



.blog_news {
    display: flex;
    flex-direction: row-reverse;
    justify-content: center;
}

.blog_news__item {
    padding-left: 10px;
}

.blog_news__reconstruct {
    padding-top: 50px;
    text-align: center;
    border-radius: 40px;
    background-color: #F4F0EC;
    height: 200px;
    margin-bottom: 50px;
}

.blog_news__text__reconstruct {
    color: #CDA274;
    font-family: "Jost", sans-serif;
    font-weight: 400;
    font-style: normal;
    width: 510px;
    text-align: center;
    padding-left: 293px;
}

.blog_news__title {
    font-family: "DM Serif Display", serif;
    font-size: 55px;
    font-weight: 400;
    font-style: normal;
    padding-bottom: 20px;
}

.blog_news__text {
    font-family: "Jost", sans-serif;
    font-size: 22px;
    font-weight: 400;
    font-style: normal;

}

.blog_news__block {
    display: flex;
    align-items: flex-end;
    flex-direction: row;
    justify-content: space-evenly;
    gap: 380px;
    padding-top: 35px;
    padding-bottom: 30px;
}





.footer {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-left: 65px;
    margin-top: 200px;
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

ol {
    font-family: "Jost", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
    list-style: none;
}
</style>