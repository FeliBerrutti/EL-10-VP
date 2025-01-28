<template>
    <div id="contactUsContainer">
            <div id="contactUsOptionsContainer">
                <div class="contactUsOption" v-for="(x, index) in contactUsOptionsText" 
                :key="index" @click="handleContactUsOptionClick(index)">
                    <div class="contactUsOptionIcon">
                        <img :src="handleContactUsIMG(index)" alt="">
                    </div>
                    <div class="contactUsOptionText"> 
                        {{ handleContactUsText(index) }}
                    </div>
                </div>
            </div>
        </div>
</template>

<style scoped>
    #contactUsContainer{
        width: 100%;
        height: 100%;
        padding: 1%;
    }

    #contactUsTitle{
        width: 90%;
        text-align: center;
        overflow: hidden;
        margin-top: 20%;
    }

    #contactUsOptionsContainer{
        width: 100%;
        height: 70%;
        padding: 1%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    .contactUsOption{
        border: 4px solid white;
        background: linear-gradient(to right, rgba(10,10,10,0.5), 
                                                rgba(150,150,150,0.5),
                                              rgba(10,10,10,0.5));
        border-radius: 20px;
        width: 40%;
        padding: 1%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin-right: 3%;
        margin-left: 3%;
    }

    .contactUsOption:hover{
        cursor: pointer;
        background-color: black;  
    }

    .contactUsOptionIcon{
        width: 80%;
        padding: 1%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .contactUsOptionIcon img{
        width: 100%;
        height: 100%;
    }

    .contactUsOptionText{
        width: 95%;
        padding: 1%;
        margin-top: 7%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    @media(max-width: 320px){
        #contactUsContainer{
            min-height: 530px;
            max-height: 580px;
        }

        #contactUsTitle{
            min-height: 50px;
            max-height: 50px;
        }

        #contactUsOptionsContainer{
            min-height: 500px;
        }

        .contactUsOption{
            min-height: 150px;
            max-height: 150px;
        }

        .contactUsOptionIcon{
            min-height: 80px;
            max-height: 80px;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 150%;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){
        #contactUsTitle{
            max-width: 300px;
            min-height: 50px;
            max-height: 50px;
            font-size: 118%;
        }

        #contactUsOptionsContainer{
            min-height: 550px;
            max-height: 600px;
        }

        .contactUsOption{
            min-height: 150px;
            max-height: 200px;
            max-width: 150px;
        }

        .contactUsOptionIcon{
            min-height: 70px;
            max-height: 70px;
            margin-top: 10%;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 150%;
            margin-top: 20%;
        }
    }

    @media(min-width: 481px) and (max-width: 768px){
        #contactUsTitle{
            max-width: 450px;
            min-height: 50px;
            max-height: 70px;
            font-size: 150%;
            margin-top: 10%;
        }

        #contactUsOptionsContainer{
            min-height: 550px;
            max-height: 600px;
        }

        .contactUsOption{
            min-height: 200px;
            max-height: 200px;
            max-width: 190px;
        }

        .contactUsOptionIcon{
            min-height: 70px;
            max-height: 70px;
            margin-top: 10%;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 220%;
            margin-top: 28%;
        }
    }

    @media(min-width: 769px) and (max-width: 960px){
        #contactUsTitle{
            max-width: 600px;
            min-height: 50px;
            max-height: 90px;
            font-size: 200%;
            margin-top: 5%;
        }

        #contactUsOptionsContainer{
            min-height: 600px;
            max-height: 600px;
        }

        .contactUsOption{
            min-height: 250px;
            max-height: 250px;
            max-width: 220px;
        }

        .contactUsOptionIcon{
            min-height: 70px;
            max-height: 70px;
            margin-top: 10%;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 255%;
            margin-top: 35%;
        }
    }

    @media(min-width: 961px) and (max-width: 1024px){
        #contactUsTitle{
            max-width: 600px;
            min-height: 50px;
            max-height: 90px;
            font-size: 200%;
            margin-top: 5%;
        }

        #contactUsOptionsContainer{
            min-height: 600px;
            max-height: 600px;
        }

        .contactUsOption{
            min-height: 250px;
            max-height: 250px;
            max-width: 220px;
        }

        .contactUsOptionIcon{
            min-height: 70px;
            max-height: 70px;
            margin-top: 10%;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 255%;
            margin-top: 35%;
        }
    }

    @media(min-width: 1025px) and (max-width: 1328px){
        #contactUsTitle{
            max-width: 750px;
            min-height: 50px;
            max-height: 110px;
            font-size: 250%;
            margin-top: 5%;
        }

        #contactUsOptionsContainer{
            min-height: 600px;
            max-height: 600px;
            margin-top: 3%;
        }

        .contactUsOption{
            min-height: 300px;
            max-height: 300px;
            max-width: 250px;
        }

        .contactUsOptionIcon{
            min-height: 70px;
            max-height: 70px;
            margin-top: 10%;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 300%;
            margin-top: 45%;
        }
    }

    @media(min-width: 1329px){
        #contactUsTitle{
            max-width: 750px;
            min-height: 50px;
            max-height: 110px;
            font-size: 250%;
            margin-top: 5%;
        }

        #contactUsOptionsContainer{
            min-height: 600px;
            max-height: 600px;
            margin-top: 3%;
        }

        .contactUsOption{
            min-height: 300px;
            max-height: 300px;
            max-width: 250px;
        }

        .contactUsOptionIcon{
            min-height: 70px;
            max-height: 70px;
            margin-top: 10%;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 300%;
            margin-top: 45%;
        }
    }
</style>

<script setup>

    import { defineEmits } from 'vue';
    import mailIcon from '@/assets/MAIL.png';
    import wppIcon from '@/assets/WPP.png';

    const emit = defineEmits();

    const contactUsOptionsText = ['Mail','Whatsapp'];
    const contactUsOptionIcon = [mailIcon, wppIcon];

    function handleContactUsIMG(aux){
        return contactUsOptionIcon[aux];
    };

    function handleContactUsText(aux){
        return contactUsOptionsText[aux];
    };

    function toggleComponent(component){
        emit('changeVisibility', component);
    };

    function handleContactUsOptionClick(index){
        index === 0 ?
        toggleComponent('isContactUsMailVisible') :
        window.open('https://wa.me/541157381951', '_blank')
    }
</script>