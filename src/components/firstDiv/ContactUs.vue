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
        border-radius: 20px;
        width: 45%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin-right: 3%;
        margin-left: 3%;
        background: linear-gradient(to right, rgba(10,10,10,0.5), 
                                                rgba(150,150,150,0.5),
                                              rgba(10,10,10,0.5));
    }

    .contactUsOption:hover{
        cursor: pointer;
        background-color: black;  
    }

    .contactUsOptionIcon{
        width: 80%;
        padding: 0.1%;
    }

    .contactUsOptionIcon img{
        width: 100%;
        height: 100%;
    }

    .contactUsOptionText{
        width: 90%;
        padding: 1%;
        text-overflow: ellipsis;
        white-space: nowrap;
        margin-top: 15%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
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

        .followUsOption{
            min-height: 150px;
            max-height: 150px;
        }

        .contactUsOptionIcon{
            min-height: 85px;
            max-height: 85px;
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
            padding: 0.1%;
        }

        .contactUsOption{
            min-width: 145px;
            max-width: 200px;
            min-height: 180px;
            max-height: 250px;
            margin: 0.3%;
        }

        .contactUsOptionIcon{
            min-height: 90px;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 190%;
            margin-top: 5%;
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
            padding: 0.1%;
        }

        .contactUsOption{
            min-width: 145px;
            max-width: 300px;
            min-height: 180px;
            max-height: 350px;
        }

        .contactUsOptionIcon{
            margin-top: 5%;
            min-height: 90px;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 300%;
            margin-top: 20%;
            margin-bottom: 10%;
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
            min-height: 450px;
            max-height: 500px;
            min-width: 320px;
            max-width: 550px;
        }

        .contactUsOptionIcon{
            min-height: 90px;
            margin-bottom: -3%;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 350%;
            margin-top: 15%;
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
            min-height: 500px;
            max-height: 550px;
            min-width: 320px;
            max-width: 550px;
        }

        .contactUsOptionIcon{
            min-height: 90px;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 400%;
            margin-top: 10%;
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
            min-height: 600px;
            max-height: 620px;
            min-width: 320px;
            max-width: 550px;
            margin-top: 3%;
        }

        .contactUsOptionIcon{
            min-height: 90px;
        }

        .contactUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 400%;
            margin-top: 10%;
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
        min-height: 600px;
        max-height: 620px;
        min-width: 320px;
        max-width: 550px;
        margin-top: 3%;
    }

    .contactUsOptionIcon{
        min-height: 90px;
    }   

    .contactUsOptionText{
        min-height: 25px;
        max-height: 25px;
        font-size: 400%;
        margin-top: 10%;
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