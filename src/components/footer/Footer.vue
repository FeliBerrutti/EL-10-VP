<template>
    <div id="footerContainer">
        <!-- DIV CONTACTANOS -->
        <div class="footerContent">
            <div class="footerContentTitle">
                <b>Contactanos</b>
            </div>
            <div class="footerOption" v-for="(x, index) in contactUsOptions" 
            :key="index" @click="handleContactUsClick(index)">
                <div class="footerIcon">
                    <img :src="handleContactUsIcon(index)" alt="">
                </div>
                <div class="footerText">
                    {{ x }}
                </div>
            </div>
        </div>
        <hr>
        <!-- DIV DONDE ESTAMOS -->
        <div class="footerContent">
            <div class="footerContentTitle">
                <b>Donde estamos</b>
            </div>
            <div class="footerOption" v-for="(x, index) in zoneList" :key="index">
                <div class="footerIcon">
                    <img :src="icon" alt="">
                </div>
                <div class="footerText">
                    {{ x }}
                </div>
            </div>
        </div>
        <hr>
        <!-- DIV SEGUINOS -->
        <div class="footerContent">
            <div class="footerContentTitle">
                <b>Seguinos</b>
            </div>
            <div class="footerOption" v-for="(x, index) in followUsOptions" 
            :key="index" @click="handleFollowUsClick(index)">
                <div class="footerIcon">
                    <img :src="handleFollowUsIcon(index)" alt="">
                </div>
                <div class="footerText">
                    {{ x }}
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    #footerContainer{
        border: 2px solid black;
        border-radius: 20px;
        width: 100%;
        padding: 0.1%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin-top: 7%;
        color: white;
        background: rgba(10,10,10,0.9);
    }

    #footerContainer hr{
        width: 80%;
        box-shadow: 2px 2px 1px 1px rgba(100,100,100,0.7);
    }

    .footerContent{
        width: 90%;
        height: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin: 2%;
    }

    .footerContentTitle{
        width: 45%;
        text-align: center;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    .footerOption{
        width: 60%;
        display: flex;
        flex-direction: row;
        align-items: center;
        margin: 2%
    }

    .footerOption:hover{
        cursor: pointer;
    }

    .footerIcon{
        width: 15%;
        margin-right: 2%;
    }

    .footerIcon img{
        width: 100%;
        height: 100%;
    }

    .footerText{
        width: 78%;
        padding: 0.1%;
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    @media(max-width: 320px){
        #footerContainer{
            min-height: 470px;
            max-height: 470px;
        }

        .footerOption{
            min-height: 25px;
        }

        .footerIcon{
            min-height: 22px;
            max-height: 22px;
        }

        .footerText{
            min-height: 24px;
            max-height: 24px;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){
        #footerContainer{
            min-height: 470px;
            max-height: 600px;
        }

        .footerContent{
            max-width: 200px;
        }

        .footerOption{
            min-height: 35px;
            min-width: 150px;
        }

        .footerIcon{
            min-height: 22px;
            max-height: 22px;
        }

        .footerText{
            min-height: 24px;
            max-height: 24px;
        }
    }

    @media(min-width: 481px) and (max-width: 550px){
        #footerContainer{
            min-height: 500px;
            max-height: 600px;
        }

        #footerContainer hr{
            max-width: 400px;
        }

        .footerContent{
            min-height: 150px;
            max-width: 300px;
            margin: 0;
        }

        .footerOption{
            min-height: 40px;
            max-height: 40px;
            min-width: 100px;
            max-width: 140px;
            margin: 0;

        }

        .footerIcon{
            min-height: 22px;
            max-height: 40px;
            min-width: 25px;
            max-width: 25px;
        }

        .footerText{
            min-height: 24px;
            max-height: 24px;
        }
    }

    @media(min-width: 551px) and (max-width: 1024px){

        #footerContainer hr{
            display: none;
        }

        #footerContainer{
            min-height: 300px;
            max-height: 300px;
            flex-direction: row;
        }

        .footerContent{
            min-height: 250px;
            min-width: 155px;
            max-width: 200px;
        }

        .footerOption{
            min-height: 40px;
            max-height: 40px;
            min-width: 150px;
        }

        .footerIcon{
            min-height: 22px;
            max-height: 40px;
            min-width: 25px;
            max-width: 25px;
        }

        .footerText{
            min-height: 24px;
            max-height: 24px;
        }
    }

    @media(min-width: 1025px) and (max-width: 1328px){

        #footerContainer hr{
            display: none;
        }

        #footerContainer{
            min-height: 300px;
            max-height: 300px;
            flex-direction: row;
        }

        .footerContent{
            min-height: 250px;
            min-width: 155px;
            max-width: 250px;
        }

        .footerOption{
            min-height: 40px;
            max-height: 40px;
            min-width: 150px;
        }

        .footerIcon{
            min-height: 22px;
            max-height: 40px;
            min-width: 25px;
            max-width: 25px;
        }

        .footerText{
            min-height: 24px;
            max-height: 24px;
        }
    }

    @media(min-width: 1328px){

        #footerContainer hr{
            display: none;
        }

        #footerContainer{
            min-height: 300px;
            max-height: 300px;
            flex-direction: row;
        }

        .footerContent{
            min-height: 250px;
            min-width: 155px;
            max-width: 250px;
        }

        .footerOption{
            min-height: 40px;
            max-height: 40px;
            min-width: 150px;
        }

        .footerIcon{
            min-height: 22px;
            max-height: 40px;
            min-width: 25px;
            max-width: 25px;
        }

        .footerText{
            min-height: 24px;
            max-height: 24px;
        }
    }
</style>

<script setup>
    import icon from '@/assets/aprobado.png';
    import mailIcon from '@/assets/MAIL.png';
    import wppIcon from '@/assets/footerWPP.png'
    import mapsIcon from '@/assets/footerMAPS.png';
    import igIcon from '@/assets/footerIG.png';
    import fbIcon from '@/assets/footerFB.png'


    const zoneList = ['Villa Devoto','Villa Urquiza','Villa Pueyrredón','Villa del Parque'];
    const contactUsOptions = ['outlook','11-5738-1951'];
    const contactUsIcons = [mailIcon,
                            wppIcon];
    const followUsOptions = ['Maps','Instagram','Facebook'];
    const followUsIcons = [mapsIcon,
                            igIcon,
                            fbIcon];

    function handleContactUsIcon(auxIndex){
        return this.contactUsIcons[auxIndex];
    };

    function handleFollowUsIcon(auxIndex){
        return this.followUsIcons[auxIndex];
    };

    function handleContactUsClick(index){
        index === 0 ?
        console.log('Mostrar contactanos mail') :
        window.open('https://wa.me/541157381951', '_blanked')
    }

    function handleFollowUsClick(index){
        index === 0 ?
        window.open('https://www.google.com/maps/dir//el+10+de+villa+pueyrredon/data=!4m6!4m5!1m1!4e2!1m2!1m1!1s0x95bcb65260679e8d:0xddf134cf27df97f4?sa=X&ved=1t:3061&ictx=111', '_blanked') :
        index === 1 ?
        window.open('https://www.instagram.com', '_blanked') :
        window.open('https://www.facebook.com', '_blanked')
    };
</script>