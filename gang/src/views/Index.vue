<template>
    <div class="_content">
        <div class="container" id="container" :class="show?'show-nav':''">
            <div class="content">
                <h1>Amazing Article</h1>
                <small>by Florin Pop 🤪</small>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Exercitationem facilis distinctio nisi! Vel eius ab sequi repellendus reiciendis voluptatum id qui dolores earum incidunt nulla, molestias quam quidem dicta odit fuga ratione provident natus quibusdam dolor labore est. Illum nisi voluptatem esse nostrum ipsa accusamus perspiciatis vel quaerat labore in natus voluptatum, sequi harum libero, et cumque nesciunt reiciendis voluptates laudantium deserunt. Placeat aliquid neque commodi nostrum necessitatibus? Accusamus ullam vel ea nesciunt sint suscipit laboriosam eos saepe ducimus quo, nam perspiciatis exercitationem laborum deleniti facilis pariatur minima rem maiores neque fugiat quae rerum, recusandae soluta magni. Praesentium, sed nostrum?</p>
                <p>Illum error officiis voluptate maiores consequatur, ad, ducimus magni impedit libero officia dolorum eum nesciunt doloribus exercitationem sunt pariatur excepturi adipisci cumque natus rem tempora accusamus rerum velit sequi. Tempora magni quasi sunt placeat officia rem porro repudiandae optio corrupti aut quam nihil inventore sit, totam quibusdam dolorem, minus eius, expedita architecto quisquam vero pariatur incidunt. Officiis libero exercitationem eveniet modi. Quos enim quasi sit praesentium aut minima maiores doloremque odio magnam culpa, magni cupiditate harum dolorum. Necessitatibus qui rerum consequatur officia amet, aspernatur officiis tempora labore ab. Error, eum asperiores! Consequatur deserunt dolorem aut accusamus cum eius rerum veniam?</p>
                <h3>Look a cute doggie! 🥰</h3>
                <img src="../assets/img/41.jpg" alt="doggy" />
                <p>Maiores, necessitatibus! Deserunt culpa ullam repudiandae pariatur nisi qui veniam nobis, consectetur iste laudantium modi dolores totam quos ratione ipsum aspernatur iure optio? Itaque tenetur nemo aspernatur eveniet maiores, laudantium sequi odio repellat perferendis voluptas. Necessitatibus impedit esse aliquid vero aut quibusdam, culpa iste delectus consectetur quasi cumque, iure distinctio blanditiis, adipisci voluptatum veniam. Maxime iste illo praesentium natus ex? Sapiente dicta rerum dignissimos omnis porro obcaecati quidem fugit. Sit commodi dolor doloribus distinctio odit quaerat possimus asperiores provident aliquam! Magni laboriosam quo quisquam earum accusamus fuga aut tempore labore quos dolorum nobis fugiat cupiditate alias sit, quasi numquam deserunt!</p>
            </div>
        </div>
        <div class="new_btn">
            <div class="circle-container">
                <div class="circle">
                    <button id="close" @click="show = false" :class="show?'no_btn':''">
                        <i class="iconfont icon-cha" style="font-size:26px"></i>
                    </button>
                    <button id="open" @click="show = true" :class="show?'get_btn':''">
                        <i class="iconfont icon-daohang" style="font-size:26px"></i>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            show:false,
            showBtn:false,
        }
    },
    methods: {
    },
}
</script>
<style lang="scss">
    @import url('https://fonts.googleapis.com/css?family=Muli&display=swap');
    @import url('https://fonts.googleapis.com/css?family=Lato&display=swap');
    ._index{display: flex;}
    .get_btn{
        transform-origin: left top;
        transform: rotate(-90deg) !important;
        transition: transform 0.5s linear;
    }
    .no_btn{
        transform-origin: left top;
        transform: rotate(0deg) !important;
        transition: transform 0.5s linear;
    }
    .header_box{
        width: 30%;
        text-align: center;
        padding: 30px 0;
        & img{width: 60px;height: 60px;border-radius: 50%;}
    }
    ._content{position: absolute;z-index: 4;width:1200px;height: 100%;top: 0;left:calc((100% - 1200px)/2);}

    * {
        box-sizing: border-box;
    }

    body {
        background-color: #333;
        /* color: #222; */
        font-family: 'Lato', sans-serif;
        margin: 0;
        overflow-x:hidden;
    }

    .container {
        // background-color: #fafafa;
        transform-origin: top left;
        transition: transform 0.5s linear;
        padding: 50px;
        min-height: 100vh;overflow-y: scroll;
        height: 100%;
        position: relative;
    }
    .new_btn{
        position: absolute;
        top: 0px;
        left: 0;
        width: 100px;
    }
    .circle-container {
        // position: fixed;
        // top: -100px;
        // left: -100px;
        // position: absolute;
        // top: -100px;
        // left: -100px;
    }

    .container.show-nav {
        transform: rotate(-20deg);
    }
    .show-btn{
        transform-origin: left top;
        transform: rotate(0);
    }
    .circle {
        background-color: #ff7979;
        /* border-radius: 50%; */
        border-radius: 0 0 100% 0;
        position: relative;
        height: 100px;
        width: 100px;
        transition: transform 0.5s linear;
        overflow: hidden;
    }

    .container.show-nav .circle {
        transform: rotate(-70deg);
    }
    .circle button {
        background: transparent; 
        border: 0;
        color: #fff;
        font-size: 26px;
        position: absolute;
        top: 0;
        left: 17px;
        height: 100px;
    }

    .circle button:focus {
        outline: none;
    }

    .circle button#open {
        left: 17px;
        transform: rotate(0deg);
        transform-origin: top left;
        transition: transform 0.5s linear;
    }

    .circle button#close {
        // top: 60%;
        transform: rotate(64deg);
        transform-origin: top left;
        transition: transform 0.5s linear;
    }

    nav {
        color: #fff;
        position: fixed;
        bottom: 40px;
        left: 0;
        z-index: 100;
    }

    nav ul {
        list-style-type: none;
        padding-left: 30px;
    }

    nav ul li {
        margin: 40px 0;
        text-transform: uppercase;
        transform: translateX(-100%);
        transition: transform 0.4s cubic-bezier(.28,.27,.65,1.25);
        transition-delay: 0s;
    }

    .container.show-nav + nav li {
        transform: translateX(0);
        transition-delay: 0.3s;
    }

    .container.show-nav + nav li a{
        color:#fff;
        text-decoration:none;
    }

    nav ul li i {
        font-size: 20px;
        margin-right: 10px;
    }

    nav ul li + li {
        margin-left: 15px;
        transform: translateX(-150%);
    }

    nav ul li + li + li {
        margin-left: 30px;
        transform: translateX(-200%);
    }


    .content {
        max-width: 1000px;
        margin: 50px auto;
    }

    .content h1 {
        margin: 0;
    }

    .content small {
        color: #555;
        font-style: italic;
    }

    .content p {
        color: #333;
        line-height: 1.5;
    }

    .content img {
        max-width: 100%;
    }

    /* SOCIAL PANEL CSS */
    .social-panel-container {
        position: fixed;
        right: 0;
        bottom: 80px;
        transform: translateX(100%);
        transition: transform 0.4s ease-in-out;
    }

    .social-panel-container.visible {
        transform: translateX(-10px);
    }

    .social-panel {	
        background-color: #fff;
        border-radius: 16px;
        box-shadow: 0 16px 31px -17px rgba(0,31,97,0.6);
        border: 5px solid #001F61;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-family: 'Muli';
        position: relative;
        height: 169px;	
        width: 370px;
        max-width: calc(100% - 10px);
    }

    .social-panel button.close-btn {
        border: 0;
        color: #97A5CE;
        cursor: pointer;
        font-size: 20px;
        position: absolute;
        top: 5px;
        right: 5px;
    }

    .social-panel button.close-btn:focus {
        outline: none;
    }

    .social-panel p {
        background-color: #001F61;
        border-radius: 0 0 10px 10px;
        color: #fff;
        font-size: 14px;
        line-height: 18px;
        padding: 2px 17px 6px;
        position: absolute;
        top: 0;
        left: 50%;
        margin: 0;
        transform: translateX(-50%);
        text-align: center;
        width: 235px;
    }

    .social-panel p i {
        margin: 0 5px;
    }

    .social-panel p a {
        color: #FF7500;
        text-decoration: none;
    }

    .social-panel h4 {
        margin: 20px 0;
        color: #97A5CE;	
        font-family: 'Muli';	
        font-size: 14px;	
        line-height: 18px;
        text-transform: uppercase;
    }

    .social-panel ul {
        display: flex;
        list-style-type: none;
        padding: 0;
        margin: 0;
    }

    .social-panel ul li {
        margin: 0 10px;
    }

    .social-panel ul li a {
        border: 1px solid #DCE1F2;
        border-radius: 50%;
        color: #001F61;
        font-size: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 50px;
        width: 50px;
        text-decoration: none;
    }

    .social-panel ul li a:hover {
        border-color: #FF6A00;
        box-shadow: 0 9px 12px -9px #FF6A00;
    }

    .floating-btn {
        border-radius: 26.5px;
        background-color: #001F61;
        border: 1px solid #001F61;
        box-shadow: 0 16px 22px -17px #03153B;
        color: #fff;
        cursor: pointer;
        font-size: 16px;
        line-height: 20px;
        padding: 12px 20px;
        position: fixed;
        bottom: 20px;
        right: 20px;
        z-index: 999;
    }

    .floating-btn:hover {
        background-color: #ffffff;
        color: #001F61;
    }

    .floating-btn:focus {
        outline: none;
    }

    @media screen and (max-width: 480px) {

        .social-panel-container.visible {
            transform: translateX(0px);
        }
        
        .floating-btn {
            right: 10px;
        }
    }
</style>