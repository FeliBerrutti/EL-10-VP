<template>
<div id="presentation">
            <div id="presentationTitle">
                <h2><b>El 10 de Villa Pueyrredón</b></h2>
            </div>
            <div id="presentationSubtitle">
                <h3><b>Alquiler de Volquetes en</b></h3>
            </div>
            <div id="presentationContentBox">
                <div class="presentationContent" v-for="(x, index) in presentationZoneList" :key="index">
                    <div class="presentationIcon">
                        <img :src="icon" alt="">
                    </div>
                    <div class="presentationText">
                        {{ x }}
                    </div>
                </div>
            </div>
        </div>
</template>

<style scoped>
    #presentation{
        width: 100%;
        height: 100%;
        padding: 0.5%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #presentationTitle{
        width: 95%;
        text-align: center;
        padding: 0.2%;
        height: 9%;
        margin-top: 10%;
    }

    #presentationSubtitle{
        width: 90%;
        height: 7%;
        padding: 0.2%;
        text-align: center;
    }

    #presentationContentBox{
        width: 100%;
        padding: 0.2%;
        height: 82%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .presentationContent{
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 90%;
        height: 10%;
        padding: 1%;
        margin-top: 10%;
    }

    .presentationIcon{
        width: 20%;
        height: 100%;
        padding: 0.1%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .presentationIcon img{
        width: 100%;
        height: 100%;
    }

    .presentationText{
        width: 80%;
        height: 100%;
        padding: 0.1%;
        text-align: center;
        display: flex;
        flex-direction: row;
        align-items: center;

    }

    @media(max-width: 320px){
        .presentationText{
            min-height: 40px;
            max-height: 50px;
            font-size: 150%;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){
        #presentationTitle{
        font-size: 115%;
        min-width: 300px;
        max-width: 500px;
        min-height: 70px;
        max-height: 70px;
    }

    #presentationSubtitle{
        font-size: 125%;
        min-height: 50px;
        max-height: 50px;
    }

    .presentationContent{
        font-size: 200%;
        margin-top: 2%;
        font-size: 180%;
    }

    .presentationText{
            min-height: 59px;
            max-height: 60px;
            font-size: 110%;
        }

    .presentationIcon{
        min-height: 59px;
        max-height: 60px;
    }
    }

    @media(min-width: 481px) and (max-width: 768px){
    #presentationTitle{
        font-size: 150%;
        min-width: 300px;
        max-width: 600px;
        min-height: 90px;
        max-height: 90px;
        margin-top: 2%;
    }

    #presentationSubtitle{
        font-size: 160%;
        min-width: 350px;
        max-width: 400px;
        min-height: 50px;
        max-height: 50px;
        margin-bottom: 2%;
    }

    .presentationContent{
        font-size: 300%;
        min-width: 500px;
        max-width: 500px;
        min-height: 80px;
        max-height: 80px;
        margin-top: 1%;
    }

    .presentationText{
            min-height: 59px;
            max-height: 80px;
            font-size: 115%;
        }

    .presentationIcon{
        min-height: 59px;
        max-height: 65px;
    }
    }

    @media(min-width: 769px) and (max-width: 960px){
    #presentationTitle{
        font-size: 200%;
        min-width: 500px;
        max-width: 600px;
        min-height: 100px;
        max-height: 100px;
        margin-top: 2%;
    }

    #presentationSubtitle{
        font-size: 150%;
        max-width: 400px;
        min-height: 50px;
        max-height: 70px;
    }

    .presentationContent{
        font-size: 400%;
        min-height: 90px;
        max-height: 90px;
        max-width: 550px;
        margin-top: 1%;
    }
    }

    @media(min-width: 961px) and (max-width: 1024px){
    #presentationTitle{
        font-size: 200%;
        min-width: 300px;
        max-width: 850px;
        min-height: 70px;
        max-height: 100px;
    }

    #presentationSubtitle{
        font-size: 150%;
        min-height: 50px;
        max-height: 70px;
    }

    .presentationContent{
        font-size: 350%;
        min-height: 70px;
        max-height: 70px;
        max-width: 500px;
        margin-top: 2%;
    }    

    .presentationIcon{
        min-height: 70px;
        max-height: 70px;
    }
    }

    @media(min-width: 1025px) and (max-width: 1328px){
    #presentationTitle{
        font-size: 200%;
        min-width: 300px;
        max-width: 700px;
        min-height: 70px;
        max-height: 100px;
    }

    #presentationSubtitle{
        font-size: 150%;
        min-width: 500px;
        max-width: 600px;
        min-height: 50px;
        max-height: 60px;
    }

    .presentationContent{
        font-size: 300%;
        min-width: 600px;
        max-width: 500px;
        min-height: 65px;
        max-height: 65px;
        margin-top: 1%;
    }

    .presentationIcon{
        max-height: 60px;
        max-width: 80px;
    }
    }


    @media(min-width: 1025px) and (max-width: 1328px){
    #presentationTitle{
        margin-top: 2%;
        font-size: 200%;
        min-width: 300px;
        max-width: 700px;
        min-height: 70px;
        max-height: 100px;
    }

    #presentationSubtitle{
        font-size: 150%;
        min-width: 500px;
        max-width: 600px;
        min-height: 50px;
        max-height: 60px;
    }

    .presentationContent{
        font-size: 300%;
        min-width: 600px;
        max-width: 500px;
        min-height: 65px;
        max-height: 65px;
        margin-top: 1%;
    }

    .presentationIcon{
        max-height: 60px;
        max-width: 80px;
    }
    }

    @media(min-width: 1329px){
    #presentationTitle{
        margin-top: 2%;
        font-size: 200%;
        min-width: 300px;
        max-width: 700px;
        min-height: 70px;
        max-height: 100px;
    }

    #presentationSubtitle{
        font-size: 150%;
        min-width: 500px;
        max-width: 600px;
        min-height: 50px;
        max-height: 60px;
    }

    .presentationContent{
        font-size: 300%;
        min-width: 600px;
        max-width: 500px;
        min-height: 65px;
        max-height: 65px;
        margin-top: 1%;
    }

    .presentationIcon{
        max-height: 60px;
        max-width: 80px;
    }
    }
</style>

<script setup>
    import icon from '@/assets/aprobado.png';

    const presentationZoneList = ['Villa Devoto','Villa del Parque',
    'Villa Urquiza','Villa Pueyrredón'];
</script>