<template>
    <div id="servicesContainer">
        <div id="aboutUsContainer">
            <div id="aboutUsTitle">
                <h2><b>¿Quienes somos?</b></h2>
            </div>
            <div id="aboutUsContent">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores ipsa dolorem officia fugit, saepe fuga! Inventore voluptatibus ad pariatur quas, veritatis labore vitae quis ipsa quaerat assumenda. Omnis, sit rem.
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Doloremque blanditiis, illum est tempore temporibus magni perspiciatis itaque voluptatum, alias, deleniti vel quam beatae accusantium! Reiciendis fugiat magni a veniam ipsa.
                </p>
            </div>
        </div>
        <div id="servicesCarrousellContainer">
            <button class="carrousellButton" @click="handleCarroussellButtonLeft(auxCarrousell)"></button>
            <div id="servicesCarrousell">
                <div id="carrousellIMG">
                    <img :src="handleCarrousellIMG()" alt="">
                </div>
            </div>
            <button class="carrousellButton" @click="handleCarrousellButtonRight(auxCarrousell)"></button>
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
        padding: 0.1%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    #servicesCarrousell{
        border: 2px solid black;
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
        border: 2px solid black;
        border-radius: 100%;
        width: 10%;
        padding: 1%;
    }
    

    .carrousellButton:hover{
        cursor: pointer;
    }

    @media(max-width: 320px){
        #servicesContainer{
            min-height: 570px;
            max-height: 570px;
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
        }

        #aboutUsContainer{
            min-height: 250px;
            max-height: 250px;
        }

        #aboutUsContent{
            min-height: 170px;
            max-height: 175px;
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
            max-width: 500px;
            min-height: 235px;
            max-height: 280px;
        }

        #servicesCarrousell{
            min-height: 190px;
            max-height: 250px;
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
            min-height: 500px;
            max-height: 600px;
        }

        #aboutUsContainer{
            max-width: 700px;
            min-height: 170px;
            max-height: 190px;
        }

        #aboutUsContent{
            max-height: 150px;
            font-size: 100%;
        }

        #servicesCarrousellContainer{
            max-width: 500px;
            min-height: 235px;
            max-height: 280px;
        }

        #servicesCarrousell{
            min-height: 190px;
            max-height: 250px;
        }

        .carrousellButton{
            min-height: 40px;
            max-height: 50px;
            min-width: 40px;
            max-width: 40px;
        }
    }

    @media(min-width: 961px) and (max-width: 1024px){
        #servicesContainer{
            max-height: 500px;
        }

        #aboutUsContainer{
            max-width: 750px;
            min-height: 170px;
            max-height: 190px;
        }

        #aboutUsContent{
            max-height: 150px;
            font-size: 100%;
        }

        #servicesCarrousellContainer{
            max-width: 500px;
            min-height: 235px;
            max-height: 280px;
        }

        #servicesCarrousell{
            min-height: 190px;
            max-height: 250px;
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

    @media(min-width: 1025px) and (max-width: 1328px){
        #servicesContainer{
            min-height: 600px;
        }

        #aboutUsContainer{
            max-width: 900px;
            min-height: 170px;
            max-height: 190px;
        }

        #aboutUsContent{
            max-height: 150px;
            font-size: 100%;
        }

        #servicesCarrousellContainer{
            max-width: 550px;
            min-height: 360px;
        }

        #servicesCarrousell{
            min-height: 250px;
            max-height: 250px;
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

    @media(min-width: 1329px){
        #servicesContainer{
            min-height: 700px;
        }

        #aboutUsContainer{
            max-width: 1200px;
            min-height: 190px;
            max-height: 190px;
        }

        #aboutUsContent{
            min-height: 128px;
            max-width: 850px;
            font-size: 110%;
        }

        #servicesCarrousellContainer{
            min-width: 800px;
            max-width: 800px;
            min-height: 500px;
        }

        #servicesCarrousell{
            min-height: 400px;
            max-height: 400px;
            min-width: 800px;
            max-width: 800px;
        }

        #servicesCarrousellButtons{
            min-height: 60px;

        }

        .carrousellButton{
            min-height: 40px;
            max-height: 50px;
            min-width: 40px;
            max-width: 40px;
        }
    }
</style>

<script setup>
    import { ref } from 'vue';
    import fontIMG from '@/assets/font.jpg';
    import truckImg from '@/assets/truck.jpg';
    import wppIMG from '@/assets/wppLogo.png'

    const auxCarrousell = ref(0);

    const servicesCarrousellImgs = [fontIMG,
                                    truckImg,
                                    wppIMG];
    
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