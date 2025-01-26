<template>
    <div id="followUsContainer">
            <div id="followUsOptionsContainer">
                <div class="followUsOption" v-for="(x, index) in followUsOptionsText" 
                :key="index" @click="handleFollowUsOptionClick(index)">
                    <div class="followUsOptionIcon">
                        <img :src="handleFollowUsIMG(index)" alt="">
                    </div>
                    <div class="followUsOptionText">
                        {{ handleFollowUsText(index) }}
                    </div>
                </div>
            </div>
        </div>
</template>

<style>
    #followUsContainer{
        width: 100%;
        height: auto;
        padding: 1%;
    }

    #followUsOptionsContainer{
        width: 100%;
        height: 70%;
        padding: 1%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    .followUsOption{
        border: 4px solid white;
        border-radius: 20px;
        width: 40%;
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

    .followUsOption:hover{
        background-color: black;
        cursor: pointer;
    }

    .followUsOptionIcon{
        width: 80%;
        padding: 0.1%;
    }

    .followUsOptionIcon img{
        width: 100%;
        height: 100%;
    }

    .followUsOptionText{
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

        #followUsOptionsContainer{
            min-height: 500px;
        }

        .followUsOption{
            min-height: 150px;
            max-height: 150px;
        }

        .followUsOptionIcon{
            min-height: 85px;
            max-height: 85px;
        }

        .followUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 150%;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){

        #followUsOptionsContainer{
            min-height: 550px;
            max-height: 600px;
        }

        .followUsOption{
            min-height: 200px;
            max-height: 220px;
        }

        .followUsOptionIcon{
            min-height: 90px;
        }

        .followUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 190%;
            margin-top: 5%;
        }
    }

    @media(min-width: 481px) and (max-width: 768px){

        #followUsOptionsContainer{
            min-height: 550px;
            max-height: 600px;
        }

        .followUsOption{
            min-height: 300px;
            max-height: 350px;
            min-width: 200px;
        }

        .followUsOptionIcon{
            margin-top: 5%;
            min-height: 90px;
        }

        .followUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 300%;
            margin-top: 20%;
            margin-bottom: 10%;
        }
}

    @media(min-width: 769px) and (max-width: 960px){

        #followUsOptionsContainer{
            min-height: 600px;
            max-height: 600px;
        }

        .followUsOption{
            min-height: 450px;
            max-height: 500px;
            min-width: 320px;
            max-width: 550px;
        }

        .followUsOptionIcon{
            min-height: 90px;
        }

        .followUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 350%;
            margin-top: 15%;
        }
}

@media(min-width: 961px) and (max-width: 1024px){

        #followUsOptionsContainer{
            min-height: 600px;
            max-height: 600px;
        }

        .followUsOption{
            min-height: 450px;
            max-height: 500px;
            min-width: 320px;
            max-width: 550px;
        }

        .followUsOptionIcon{
            min-height: 90px;
        }

        .followUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 400%;
            margin-top: 10%;
        }
}

@media(min-width: 1025px) and (max-width: 1328px){

        #followUsOptionsContainer{
            min-height: 600px;
            max-height: 600px;
            margin-top: 3%;
        }

        .followUsOption{
            min-height: 480px;
            max-height: 600px;
            min-width: 320px;
            max-width: 360px;
        }

        .followUsOptionIcon{
            min-height: 90px;
        }

        .followUsOptionText{
            min-height: 25px;
            max-height: 25px;
            font-size: 400%;
            margin-top: 10%;
        }
}

@media(min-width: 1329px){

#followUsOptionsContainer{
    min-height: 600px;
    max-height: 600px;
    margin-top: 3%;
}

.followUsOption{
    min-height: 480px;
    max-height: 600px;
    min-width: 320px;
    max-width: 360px;
}

.followUsOptionIcon{
    min-height: 90px;
}

.followUsOptionText{
    min-height: 25px;
    max-height: 25px;
    font-size: 400%;
    margin-top: 10%;
}
}
</style>

<script setup>
    import igIcon from '@/assets/desktopIG.png';
    import fbIcon from '@/assets/desktopFB.png';

    const followUsOptionsText = ['Instagram','Facebook'];
    const followUsOptionIcon = [igIcon, fbIcon];

    function handleFollowUsIMG(aux){
        return this.followUsOptionIcon[aux];
    };

    function handleFollowUsText(aux){
        return this.followUsOptionsText[aux];
    };

    function handleFollowUsOptionClick(index){
        index === 0 ?
        window.open('https://www.instagram.com', '_blank') :
        window.open('https://www.facebook.com', '_blank')
    };
</script>