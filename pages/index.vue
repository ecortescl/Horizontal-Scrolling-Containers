<template>
<div>
    <div class="wrapper">
        <div class="flotante p-4">
           <h3>Scrolling Div Horizontal</h3>
            <h4>FLOTANTE CONTENIDO</h4>

            <ul>
                <li class="btn btn-dark mb-2 w-100"><a href="#box1"> Box 1</a></li>
                <li class="btn btn-dark mb-2 w-100"><a href="#box2"> Box 2</a></li>
                <li class="btn btn-dark mb-2 w-100"><a href="#box3"> Box 3</a></li>
                <li class="btn btn-dark mb-2 w-100"><a href="#box4"> Box 4</a></li>
                <li class="btn btn-dark mb-2 w-100"><a href="#box5"> Box 5</a></li>
                <li class="btn btn-dark mb-2 w-100"><a href="#box6"> Box 6</a></li>
            </ul>
        </div>
        <div class="item" id="box1">box-1</div>
        <div class="item" id="box2">box-2</div>
        <div class="item" id="box3">box-3</div>
        <div class="item" id="box4">
            <Slider></Slider>
        </div>
        <div class="item" id="box5">box-5</div>
        <div class="item" id="box6">box-6</div>
    </div>

</div>
</template>

<script>
export default {
    name: 'IndexPage'
}
</script>

<style>
li{
  list-style: none;

}
a{
  color:#fff;
  text-decoration: none;
  
}

html {
    scroll-behavior: smooth;
}

.wrapper {
    max-height: 100vh;
    border: 1px solid #ddd;
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
</style>
