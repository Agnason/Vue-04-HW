<template>
    <div>
        <h2 class='textAlignLeft heading center'> {{ heading }} </h2>
        <img class='imgFitBlock' :src="imgSrc" :alt="imgAlt">
        <p class='text textAlignLeft '> {{ text }} </p>
    </div>
</template>

<script>
export default {
    name: 'ChangeArchitecture',

    data() {
        return {
            heading: 'Let’s Get Solution for Building Construction Work of Architecture',
            imgSrc: 'img/blog-architecture.jpg',
            imgAlt: 'blog-architecture',
            text: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Enim cum facilis harum nostrum placeat perspiciatis excepturi veniam aliquam repellat itaque'
        };
    },

    methods: {

    },
};
</script>

<style lang="scss">
$widthSite-laptop: 1201px;
$widthSite-laptop-center: $widthSite-laptop / 2;
$colorHeader: #292F36;
$colorText: #4D5053;
$colorWhite: #FFFFFF;
$colorBackground: #F4F0EC;
$colorCounterBlock: #CDA274;
$colorBlock: #F4F0EC;

* {
    margin: 0px;
    padding: 0px;
}

a {
    text-decoration: none;
}

.center {
    padding-left: calc(50% - $widthSite-laptop-center);
    padding-right: calc(50% - $widthSite-laptop-center);
}

.text {
    font-family: 'Jost';
    font-style: normal;
    font-weight: 400;
    font-size: 22px;
    line-height: 150%;
    letter-spacing: 0.01em;
    color: $colorText;
    text-align: center;
}

.heading {
    font-family: 'DM Serif Display';
    font-style: normal;
    font-weight: 400;
    font-size: 50px;
    line-height: 125%;
    color: $colorHeader;
    text-align: center;
}

// выравнивание текста по левому краю
.textAlignLeft {
    text-align: left;
}

.imgFitBlock {
    object-fit: cover;
    width: 100%;
    height: 100%;
}
</style>