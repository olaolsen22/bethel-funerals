<template lang="pug">
    .jumbotron.custom-image
        .container
            h1.headline Save $275 on a Prepaid Funeral*
            
</template>

<style lang="scss" scoped>
.jumbotron {
    height: 30rem;
    @media screen and (max-width: 1024px) { height: 26rem; }
    @media screen and (max-width: 425px) { 
        height: 16rem;
        padding: 0;
    }
    &.custom-image {
        background: 
            linear-gradient(
                to right, 
                #E5E5E5,
                #E5E5E5,
                #E5E5E5,
                rgba(0,0,0,0), 
                rgba(0,0,0,0), 
                rgba(0,0,0,0)
            ), 
            url("../../assets/images/landing-hero-1.png") no-repeat 100% 50%;
        @media screen and (max-width: 768px) {
            background: 
                linear-gradient(
                    to right, 
                    #E5E5E5,
                    #E5E5E5,
                    #E5E5E5,
                    rgba(0,0,0,0), 
                    rgba(0,0,0,0), 
                    rgba(0,0,0,0)
                ), 
                url("../../assets/images/landing-hero-1.png");
                background-size: cover;
                background-position: 60% 50%;
        }
    }
    .container {
        display: flex;
        align-items: center;
        height: 100%;
        @media screen and (max-width: 768px) { padding: 0; }
        @media screen and (max-width: 425px) { 
            align-items: flex-start;
            padding: 0 1rem;
        }
    }
}
.headline {
    width: 28rem;
    color: #009FC2;
    font-size: 73px;
    font-weight: bold;
    text-align: left;
    padding: 1rem 0;
    @media screen and (max-width: 1024px) {
        font-size: 60px;
        width: 23rem;
    }
    @media screen and (max-width: 768px) {
        font-size: 42px;
        width: 16rem;
    }
    @media screen and (max-width: 425px) {
        font-size: 22px;
        width: 8rem;
    }
}
</style>