<template>
    <div id="menuContainer">
        <div id="menuButton" @click="handleMenuButton">
            <hr>
            <hr>
            <hr>
        </div>
        <div id="menuOptionsContainer" v-show="isMenuVisible">
            <div class="menuOption" v-for="(x, index) in menuOptionsList"
            :key="index" @click="handleMenuOption(index)">
                <div class="menuOptionIcon">
                    <img :src="handleMenuIcon(index)" alt="">
                </div>
                <div class="menuOptionText">
                    {{ x }}
                </div>
            </div>
        </div>
    </div>
</template>

<style>
    #menuContainer{
        width: 100%;
        height: auto;
        padding: 0.1%;
        position: fixed;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        right: 1%;
        top: 0;
    }

    #menuButton{
        border: 3px solid rgb(150,150,150);
        width: 20%;
        border-radius: 10px;
        background-color: black;
        color: white;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    #menuButton:hover{
        cursor: pointer;
    }

    #menuButton hr{
        width: 65%;
        border: 2px solid rgb(150,150,150);
        box-shadow: 1px 3.5px 1px 1px rgb(70,70,70);
        border-radius: 20px;
        margin: 8%;
    }

    #menuOptionsContainer{
        border: 2px solid white;
        border-radius: 10px;
        width: 95%;
        height: auto;
        padding: 0.5%;
        background-color: black;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .menuOption{
        width: 75%;
        display: flex;
        flex-direction: row;
        align-items: center;
        margin: 2%;
        padding: 1%;
    }

    .menuOption:hover{
        cursor: pointer;
    }

    .menuOptionIcon{
        width: 20%;
        height: 100%;
        padding: 0.1%;
        margin-right: 2%;
    }

    .menuOptionIcon img{
        width: 100%;
        height: 100%;
    }

    .menuOptionText{
        width: 80%;
        height: 100%;
        padding: 0.1%;
        color: white;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    @media(max-width: 320px){
        #menuButton{
            height: 50px;
        }

        .menuOption{
            height: 40px;
            max-height: 45px;
        }

        .menuOptionText{
            font-size: 150%;
        }
    }

    @media(min-width: 321px) and (max-width:480px){
        #menuButton{
            min-height: 60px;
            max-height: 60px;
            max-width: 80px;
        }

        #menuOptionsContainer{
            min-width: 300px;
            max-width: 300px;
        }

        .menuOption{
            min-height: 38px;
            max-height: 45px;
            min-width: 200px;
            max-width: 210px;
            margin-top: 0.5%;
        }

        .menuOptionText{
            font-size: 120%;
        }
    }

    @media(min-width:481px) and (max-width: 768px){
        #menuButton{
            min-height: 75px;
            max-height: 90px;
            min-width: 90px;
            max-width: 100px;
        }

        #menuOptionsContainer{
            min-width: 300px;
            max-width: 400px;
            min-height: 300px;
            max-height: 400px;
        }

        .menuOption{
            min-height: 38px;
            max-height: 45px;
            min-width: 250px;
            max-width: 300px;
            margin-top: 3%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-left: 20%;
        }

        .menuOptionText{
            font-size: 150%;
        }

        .menuOptionIcon{
            display: none;
        }
    }

    @media(min-width: 769px) and (max-width: 960px){
        #menuButton{
            min-height: 75px;
            max-height: 90px;
            min-width: 90px;
            max-width: 100px;
        }

        #menuOptionsContainer{
            min-width: 300px;
            max-width: 400px;
            min-height: 300px;
            max-height: 400px;
        }

        .menuOption{
            min-height: 38px;
            max-height: 45px;
            min-width: 250px;
            max-width: 300px;
            margin-top: 3%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .menuOptionText{
            font-size: 150%;
            margin-left: 20%;
        }

        .menuOptionIcon{
            display: none;
        }
    }

    @media(min-width: 961px) and (max-width: 1024px){
        #menuButton{
            min-height: 75px;
            max-height: 90px;
            min-width: 90px;
            max-width: 100px;
        }

        #menuOptionsContainer{
            min-width: 300px;
            max-width: 400px;
            min-height: 300px;
            max-height: 400px;
        }

        .menuOption{
            border: 2px solid red;
            min-height: 38px;
            max-height: 45px;
            min-width: 250px;
            max-width: 300px;
            margin-top: 3%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .menuOptionText{
            font-size: 150%;
            margin-left: 20%;
        }

        .menuOptionIcon{
            display: none;
        }
    }

    @media(min-width: 1025px) and (max-width: 1328px){
        #menuButton{
            min-height: 100px;
            max-height: 130px;
            min-width: 100px;
            max-width: 120px;
        }

        #menuOptionsContainer{
            min-width: 300px;
            max-width: 400px;
            min-height: 300px;
            max-height: 400px;
        }

        .menuOption{
            min-height: 38px;
            max-height: 55px;
            min-width: 270px;
            max-width: 320px;
            margin-top: 2%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .menuOptionText{
            font-size: 190%;
        }

        .menuOptionIcon{
            display: none;
        }
    }

    @media(min-width: 1329px){
        #menuButton{
            min-height: 100px;
            max-height: 130px;
            min-width: 100px;
            max-width: 120px;
        }

        #menuOptionsContainer{
            min-width: 300px;
            max-width: 400px;
            min-height: 300px;
            max-height: 400px;
        }

        .menuOption{
            min-height: 38px;
            max-height: 55px;
            min-width: 270px;
            max-width: 320px;
            margin-top: 2%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .menuOptionText{
            font-size: 190%;
        }

        .menuOptionIcon{
            display: none;
        }
    }
</style>

<script setup>
    import { ref } from 'vue';
    import { defineEmits } from 'vue';
    import icon from '@/assets/aprobado.png';
    import mapsIcon from '@/assets/footerMAPS.png';
    import mailIcon from '@/assets/MAIL.png';
    import fbIcon from '@/assets/footerIG.png'

    const emit = defineEmits();

    const menuOptionsList = ['SERVICIOS','DIRECCION','CONTACTANOS',
    'SEGUINOS','INFORMACION','ZONAS'];

    const menuOptionsImg = [icon, mapsIcon,
                            mailIcon,fbIcon,
                            icon, mapsIcon];
    const isMenuVisible = ref(false);

    function handleMenuButton(){
                isMenuVisible.value = !isMenuVisible.value;
            };

    function handleMenuIcon(aux){
                return menuOptionsImg[aux];
            };

    function goMaps(){
        window.open('https://www.google.com/maps/dir//el+10+de+villa+pueyrredon/data=!4m6!4m5!1m1!4e2!1m2!1m1!1s0x95bcb65260679e8d:0xddf134cf27df97f4?sa=X&ved=1t:3061&ictx=111', '_blanked');
    };

    function toggleComponent(component){
        emit('changeVisibility', component);
    };

    function scrollComponent(aux){
        document.getElementById(aux).scrollIntoView({behavior : 'smooth'})
    }

    function handleMenuOption(index){
        if(index === 0){
            handleMenuButton();
            scrollComponent('servicesContainer');
        }
        else if(index === 1){
            handleMenuButton();
            scrollComponent('container');
            goMaps();
        }
        else if(index === 2){
            handleMenuButton();
            scrollComponent('container');
            toggleComponent('isContactUsVisible');
        }
        else if( index === 3){
            handleMenuButton();
            scrollComponent('container');
            toggleComponent('isFollowUsVisible');
        }
        else if(index === 4){
            handleMenuButton();
            scrollComponent('footerContainer');
        }
        else{
            handleMenuButton();
            scrollComponent('container');
            toggleComponent('presentation');
        }
    };
</script>