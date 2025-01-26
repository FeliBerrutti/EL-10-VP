<template>
<div id="wppContainer">
    <a href="https://wa.me/541157381951" target="_blank">
        <img :src="wppIcon" alt="">
    </a>
</div>
</template>

<style>
    #wppContainer{
        border-radius: 100%;
        bottom: 2%;
        right: 2%;
        position: fixed;
        width: 25%;
        background-image: url('');
        background-position: center;
        background-size: cover;
    }

    #wppContainer img{
        width: 100%;
        height: 100%;
    }

    @media(max-width: 320px){
        #wppContainer{
            height: 75px;
            max-height: 80px;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){
        #wppContainer{
            min-height: 75px;
            max-height: 120px;
            max-width: 110px;
        }
    }

    @media(min-width: 481px) and (max-width: 768px){
        #wppContainer{
            min-height: 80px;
            max-height: 120px;
            min-width: 100px;
            max-width: 120px;
        }
    }

    @media(min-width: 769px) and (max-width: 960px){
        #wppContainer{
            min-height: 80px;
            max-height: 120px;
            min-width: 100px;
            max-width: 120px;
        }
    }

    @media(min-width: 961px) and (max-width: 1024px){
        #wppContainer{
            min-height: 80px;
            max-height: 120px;
            min-width: 100px;
            max-width: 120px;
        }
    }

    @media(min-width: 1025px) and (max-width: 1328px){
        #wppContainer{
            min-height: 80px;
            max-height: 120px;
            min-width: 100px;
            max-width: 120px;
        }
    }

    @media(min-width: 1329px){
        #wppContainer{
            max-height: 120px;
            max-width: 120px;
        }
    }
</style>

<script setup>
    import wppIcon from '@/assets/wppLogo.png'
</script>