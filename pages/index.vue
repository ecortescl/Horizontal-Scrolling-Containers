<template>
<div>
    <div class="wrapper">
        <div class="flotante p-4">
            <h3>Scrolling Div Horizontal</h3>
            <h4>FLOTANTE CONTENIDO</h4>
            <ul>
                <li class=" mb-2 w-100"><a href="#box1" @click="collapseShow1()"> Titular 1</a>
                    <Transition>
                        <p v-if="show==true">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lorem lectus, suscipit cursus dictum ut, pellentesque nec augue. Suspendisse felis arcu, malesuada sed nisl et, consectetur dapibus diam</p>
                    </Transition>
                </li>
                <li class=" mb-2 w-100"><a href="#box2" @click="collapseShow2()"> Titular 2</a>
                    <Transition>
                        <p v-if="show2==true">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lorem lectus, suscipit cursus dictum ut, pellentesque nec augue. Suspendisse felis arcu, malesuada sed nisl et, consectetur dapibus diam</p>
                    </Transition>
                </li>
                <li class=" mb-2 w-100"><a href="#box3" @click="collapseShow3()"> Titular 3</a>
                    <Transition>
                        <p v-if="show3==true">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lorem lectus, suscipit cursus dictum ut, pellentesque nec augue. Suspendisse felis arcu, malesuada sed nisl et, consectetur dapibus diam</p>
                    </Transition>
                </li>
                <li class=" mb-2 w-100"><a href="#box4" @click="collapseShow4()"> Titular 4</a>
                    <Transition>
                        <p v-if="show4==true">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lorem lectus, suscipit cursus dictum ut, pellentesque nec augue. Suspendisse felis arcu, malesuada sed nisl et, consectetur dapibus diam</p>
                    </Transition>
                </li>
                <li class=" mb-2 w-100"><a href="#box5" @click="collapseShow5()"> Titular 5</a>
                    <Transition>
                        <p v-if="show5==true">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lorem lectus, suscipit cursus dictum ut, pellentesque nec augue. Suspendisse felis arcu, malesuada sed nisl et, consectetur dapibus diam</p>
                    </Transition>
                </li>
                <li class=" mb-2 w-100"><a href="#box6" @click="collapseShow6()"> Titular 6</a>
                    <Transition>
                        <p v-if="show6==true">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lorem lectus, suscipit cursus dictum ut, pellentesque nec augue. Suspendisse felis arcu, malesuada sed nisl et, consectetur dapibus diam</p>
                    </Transition>
                </li>
            </ul>
        </div>
        <div class="item" id="box1">
          <h1>CONTENIDO DEL BOX1</h1>
        </div>
        <div class="item" id="box2"><h1>CONTENIDO DEL BOX2</h1></div>
        <div class="item" id="box3"><h1>CONTENIDO DEL BOX3</h1></div>
        <div class="item" id="box4">
            <Slider></Slider>
        </div>
        <div class="item" id="box5"><h1>CONTENIDO DEL BOX5</h1></div>
        <div class="item" id="box6"><h1>CONTENIDO DEL BOX6</h1></div>
    </div>

</div>
</template>

<script>
export default {
    name: 'IndexPage',
    data() {
        return {
            show: false,
            show2: false,
            show3: false,
            show4: false,
            show5: false,
            show6: false,

        }
    },
    methods: {
        collapseShow1() {
            this.show = true;
            this.show2 = false;
            this.show3 = false;
            this.show4 = false;
            this.show5 = false;
            this.show6 = false;

        },
        collapseShow2() {
            this.show = false;
            this.show2 = true;
            this.show3 = false;
            this.show4 = false;
            this.show5 = false;
            this.show6 = false;

        },
        collapseShow3() {
            this.show = false;
            this.show2 = false;
            this.show3 = true;
            this.show4 = false;
            this.show5 = false;
            this.show6 = false;

        },
        collapseShow4() {
            this.show = false;
            this.show2 = false;
            this.show3 = false;
            this.show4 = true;
            this.show5 = false;
            this.show6 = false;

        },
        collapseShow5() {
            this.show = false;
            this.show2 = false;
            this.show3 = false;
            this.show4 = false;
            this.show5 = true;
            this.show6 = false;

        },
        collapseShow6() {
            this.show = false;
            this.show2 = false;
            this.show3 = false;
            this.show4 = false;
            this.show5 = false;
            this.show6 = true;

        },
    }
}
</script>

<style>
li {
    list-style: none;

}

a {
    color: #fff;
    text-decoration: none;

}

html {
    scroll-behavior: smooth;
}

.wrapper {
    max-height: 100vh;
    display: flex;
    overflow-x: hidden !important;
    overflow-y: hidden !important;
    scroll-behavior: smooth;

}

.wrapper ::-webkit-scrollbar {
    width: 0;
}

.wrapper .item {
    min-width: 100%;
    min-height: 100vh;
    line-height: 110px;
    text-align: center;
    overflow-x: hidden !important;
    overflow-y: hidden !important;
    scroll-behavior: smooth;
}

.flotante {
    color: #fff;
    position: absolute;
    width: 400px;
    right: 0px;
    height: 100vh;
    background: rgba(0, 0, 0, 0.50);
    overflow-x: hidden !important;
    overflow-y: hidden !important;
    z-index: 1000;
}

#box1 {
    background-color: red;
}

#box2 {
    background-color: orange;
}

#box3 {
    background-color: blue;
}

#box4 {
    background-color: darkcyan;
}

#box5 {
    background-color: yellow;
}

#box6 {
    background-color: green;
}

/* we will explain what these classes do next! */
.v-enter-active,
.v-leave-active {
    transition: opacity 0.2s ease;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}
</style>
