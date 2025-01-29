<template>
    <div id="servicesContainer">
        <div id="aboutUsContainer">
            <div id="aboutUsTitle">
                <h2><b>¿Quienes somos?</b></h2>
            </div>
            <div id="aboutUsContent">
                <p>
                    En El 10 de Villa Pueyrredón nos dedicamos al alquiler de volquetes.<br>
                    Nuestro objetivo es satisfacer tus necesidades de limpieza y transporte de residuos.<br> 
                    Limpiamos y retiramos escombros, tierra, residuos de obra, fábrica y podas. <br>
                    Ofrecemos un servicio confiable y eficiente siempre a disposición de nuestros clientes. ¡Tu satisfacción es nuestra prioridad!.
                </p>
            </div>
        </div>
        <div id="servicesCarrousellContainer">
            <button class="carrousellButton" @click="handleCarroussellButtonLeft(auxCarrousell)">
                <img :src="leftArrow" alt="">
            </button>
            <div id="servicesCarrousell">
                <div id="carrousellIMG">
                    <img :src="handleCarrousellIMG()" alt="">
                </div>
            </div>
            <button class="carrousellButton" @click="handleCarrousellButtonRight(auxCarrousell)">
                <img :src="rightArrow" alt="">
            </button>
        </div>
    </div>
</template>

<style>
    #servicesContainer{
        width: 100%;
        padding: 0.5%;
        overflow: hidden;
        margin-top: 7%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    #aboutUsContainer{
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 97%;
        padding: 1%;
    }

    #aboutUsContent{
        padding: 0.1%;
        text-align: center;
    }

    #servicesCarrousellContainer{
        border-radius: 20px;
        width: 99%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    #servicesCarrousell{
        border: 1.5px solid black;
        border-radius: 10px;
        width: 90%;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #carrousellIMG{
        width: 100%;
        height: auto;
    }

    #carrousellIMG img{
        width: 100%;
        height: 100%;
    }

    .carrousellButton{
        border: 1px solid black;
        border-radius: 10px;
        background: rgba(220,220,220,0.2);
        width: 10%;
        padding: 1%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    
    .carrousellButton img{
        width: 100%;
        height: 100%;
    }

    .carrousellButton:hover{
        cursor: pointer;
    }

    @media(max-width: 320px){
        #servicesContainer{
            min-height: 570px;
            max-height: 570px;
            margin-top: 2%;
        }

        #aboutUsContainer{
            min-height: 300px;
            max-height: 300px;
        }

        #aboutUsContent{
            min-height: 220px;
            max-height: 220px;
        }

        #servicesCarrousellContainer{
            min-height: 250px;
            max-height: 250px;
        }

        #servicesCarrousell{
            min-height: 200px;
            max-height: 200px;
        }

        #carrousellIMG img{
            min-height: 200px;
            max-height: 200px;
        }

        .carrousellButton{
            min-height: 35px;
            max-height: 35px;
            width: 13%;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){
        #servicesContainer{
            min-height: 500px;
            max-height: 500px;
            margin-top: 2%;
        }

        #aboutUsContainer{
            min-height: 235px;
            max-height: 235px;
        }

        #aboutUsContent{
            min-height: 165px;
            max-height: 150px;
            font-size: 90%;
        }

        #servicesCarrousellContainer{
            min-height: 235px;
            max-height: 250px;
        }

        #servicesCarrousell{
            min-height: 190px;
            max-height: 190px;
        }

        #carrousellIMG img{
            min-height: 190px;
            max-height: 190px;
        }


        #servicesCarrousellButtons{
            min-height: 35px;
            max-height: 35px;
        }

        .carrousellButton{
            min-height: 40px;
            max-height: 50px;
            min-width: 40px;
            max-width: 40px;
        }
    }

    @media(min-width: 481px) and (max-width: 768px){
        #servicesContainer{
            min-height: 500px;
            max-height: 530px;
            margin-top: 5%;
        }

        #aboutUsContainer{
            max-width: 500px;
            min-height: 220px;
        }

        #aboutUsContent{
            max-height: 150px;
            font-size: 100%;
        }

        #servicesCarrousellContainer{
            min-height: 300px;
            max-height: 400px;
            min-width: 380px;
            max-width: 650px;
        }

        #servicesCarrousell{
            min-height: 290px;
            max-height: 290px;
        }

        #carrousellIMG img{
            min-height: 290px;
            max-height: 290px;
        }


        #servicesCarrousellButtons{
            min-height: 35px;
            max-height: 35px;
        }

        .carrousellButton{
            min-height: 40px;
            max-height: 50px;
            min-width: 40px;
            max-width: 40px;
        }
    }

    @media(min-width: 769px) and (max-width: 960px){
        #servicesContainer{
            min-height: 600px;
            margin-top: 3%;
        }

        #aboutUsContainer{
            max-width: 700px;
            min-height: 200px;
            max-height: 250px;
            font-size: 120%;
            margin-bottom: 3%;
        }

        #aboutUsContent{
            min-height: 150px;
            max-height: 150px;
        }

        #servicesCarrousellContainer{
            min-width: 600px;
            max-width: 900px;
            min-height: 400px;
            max-height: 500px;
        }

        #servicesCarrousell{
            min-height: 350px;
            max-height: 390px;
            min-width: 630px;
            max-width: 630px;
        }

        #carrousellIMG img{
            min-height: 350px;
            max-height: 390px;
            min-width: 630px;
            max-width: 630px;
        }

        .carrousellButton{
            min-height: 50px;
            max-height: 50px;
            min-width: 50px;
            max-width: 50px;
        }
    }

    @media(min-width: 961px) and (max-width: 1024px){
        #servicesContainer{
            min-height: 900px;
            max-height: 950px;
            margin-top: 2%;
        }

        #aboutUsContainer{
            max-width: 1200px;
            min-height: 190px;
            max-height: 370px;
            font-size: 150%;
        }

        #aboutUsContent{
            min-height: 128px;
            max-height: 250px;
            max-width: 850px;
        }

        #servicesCarrousellContainer{
            min-width: 800px;
            max-width: 800px;
            min-height: 600px;
            max-height: 650px;
        }

        #servicesCarrousell{
            min-height: 550px;
            max-height: 600px;
            min-width: 790px;
            max-width: 790px;
        }   

        #carrousellIMG img{
            min-height: 550px;
            max-height: 600px;
            min-width: 790px;
            max-width: 790px;
        }

        #servicesCarrousellButtons{
            min-height: 35px;
            max-height: 35px;
        }

        .carrousellButton{
            min-height: 60px;
            max-height: 80px;
            min-width: 60px;
            max-width: 80px;
        }
    }

    @media(min-width: 1025px) and (max-width: 1328px){
        #servicesContainer{
            min-height: 600px;
            margin-top: 2%;
        }

        #aboutUsContainer{
            max-width: 1200px;
            min-height: 190px;
            max-height: 370px;
            font-size: 150%;
        }

        #aboutUsContent{
            min-height: 128px;
            max-height: 250px;
            max-width: 850px;
        }

        #servicesCarrousellContainer{
            min-width: 800px;
            max-width: 800px;
            min-height: 600px;
            max-height: 650px;
        }

        #servicesCarrousell{
            min-height: 550px;
            max-height: 600px;
            min-width: 790px;
            max-width: 790px;
        }

        #carrousellIMG img{
            min-height: 550px;
            max-height: 600px;
            min-width: 790px;
            max-width: 790px;
        }

        #servicesCarrousellButtons{
            min-height: 35px;
            max-height: 35px;
        }

        .carrousellButton{
            min-height: 60px;
            max-height: 80px;
            min-width: 60px;
            max-width: 80px;
        }
    }

    @media(min-width: 1329px){
        #servicesContainer{
            min-height: 700px;
            margin-top: 2%;
        }

        #aboutUsContainer{
            max-width: 1200px;
            min-height: 190px;
            max-height: 370px;
            font-size: 150%;
        }

        #aboutUsContent{
            min-height: 128px;
            max-height: 250px;
            max-width: 850px;
            font-size: 110%;
        }

        #servicesCarrousellContainer{
            min-width: 800px;
            max-width: 800px;
            min-height: 600px;
            max-height: 650px;
        }

        #servicesCarrousell{
            min-height: 550px;
            max-height: 600px;
            min-width: 790px;
            max-width: 790px;
        }

        #carrousellIMG img{
            min-height: 550px;
            max-height: 600px;
            min-width: 790px;
            max-width: 790px;
        }

        #servicesCarrousellButtons{
            min-height: 60px;
        }

        .carrousellButton{
            min-height: 60px;
            max-height: 80px;
            min-width: 60px;
            max-width: 80px;
        }
    }
</style>

<script setup>
    import { ref } from 'vue';
    import piletas from '@/assets/PILETAS.png';
    import podas from '@/assets/PODAS.png';
    import demoliciones from '@/assets/DEMOLICIONES.png';
    import galpones from '@/assets/GALPONES.png';
    import rightArrow from '@/assets/rightArrow.png';
    import leftArrow from '@/assets/leftArrow.png';

    const auxCarrousell = ref(0);

    const servicesCarrousellImgs = [piletas,
                                    podas,
                                    demoliciones,
                                    galpones
    ];
    
    function handleCarrousellIMG(){
        return servicesCarrousellImgs[auxCarrousell.value];
    };


    function handleCarrousellButtonRight(){
        if(auxCarrousell.value === servicesCarrousellImgs.length - 1){
            auxCarrousell.value = 0;
        }
        else{
            auxCarrousell.value++;
        }
    };

    function handleCarroussellButtonLeft(){
        if(auxCarrousell.value === 0){
            auxCarrousell.value = servicesCarrousellImgs.length - 1;
        }
        else{
            auxCarrousell.value--;
        }
    };
</script>