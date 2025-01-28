<template>
    <div id="mailFormContainer">
        <form action="" id="probForm">
            <div class="formCell">
            <div class="formLabel">
                <b>Nombre</b>
            </div>
            <div class="formInput">
                <input type="text" class="input" required>
            </div>
        </div>
        <div class="formCell">
            <div class="formLabel">
                <b>Mail</b>
            </div>
            <div class="formInput">
                <input type="email" class="input" required>
            </div>
        </div>
        <div id="textAreaContainer">
            <div id="textAreaLabel">
                <h4>Mensaje</h4>
            </div>
        <textarea name="Mensaje" id="textArea" rows="8" required></textarea>
        <button id="formSendButton">
            <b>Enviar</b>
        </button>
        </div>
        </form>
    </div>
</template>

<style scoped> 
    #mailFormContainer{
        width: 100%;
        height: 80%;
        padding: 0.1%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .formCell{
        width: 80%;
        height: 5%;
        padding: 1%;
        margin-top: 5%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;

    }

    #textAreaContainer{
        width: 90%;
        padding: 1%;
        height: 60%;
        margin-top:3%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #textAreaLabel{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .formLabel{
        width: 40%;
        height: 99%;
        padding: 0.1%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .formInput{
        width: 52%;
        height: 99%;
        padding: 0.1%;
        margin-left: 8%;
    }

    .input{
        border-radius: 10px;
        width: 100%;
        height: 80%;
    }

    #textArea{
        border-radius: 10px;
        width: 95%;
    }

    #formSendButton{
        width: 25%;
        padding: 0.5%;
        margin-top: 5%;
    }

    #formSendButton:hover{
        cursor: pointer;
    }

    #probForm{
        width: 95%;
        height: 90%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    @media(max-width: 320px){

        #mailFormContainer{
            margin-top: 20%;
            min-height: 480px;
            max-height: 580px;
        }

        .formCell{
            min-height: 25px;
            max-height: 30px;
        }

        #textAreaContainer{
            min-height: 250px;
            max-height: 250px;
        }

        #textArea{
            min-height: 130px;
            max-height: 130px;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){

        #mailFormContainer{
            margin-top: 25%;
        }

        .formCell{
            min-height: 25px;
            max-height: 30px;
        }

        #textAreaContainer{
            min-height: 250px;
            max-height: 250px;
        }

        #textArea{
            min-height: 130px;
            max-height: 130px;
        }
    }

    @media(min-width: 481px) and (max-width: 960px){

        #mailFormContainer{
            margin-top: 10%;
        }

        .formCell{
            min-height: 40px;
        }

        .formLabel{
            min-height: 40px;
            max-height: 40px;
            font-size: 160%;
        }

        .formInput{
            min-height: 40px;
            max-height: 40px;
        }

        .input{
            min-height: 30px;
            max-height: 30px;
        }

        #textAreaContainer{
            min-height: 250px;
            max-height: 250px;
        }

        #textAreaLabel{
            min-width: 200px;
            max-height: 70px;
            font-size: 160%;
        }

        #textArea{
            min-height: 130px;
            max-height: 130px;
        }

        #formSendButton{
            min-height: 35px;
            font-size: 110%;
        }
    }

    @media(min-width: 961px) and (max-width: 1024px){

        #mailFormContainer{
            margin-top: 5%;
        }

        .formCell{
            min-height: 40px;
        }

        .formLabel{
            min-height: 40px;
            max-height: 40px;
            font-size: 160%;
        }

        .formInput{
            min-height: 40px;
            max-height: 40px;
        }

        .input{
            min-height: 30px;
            max-height: 30px;
        }

        #textAreaContainer{
            min-height: 250px;
            max-height: 250px;
        }

        #textAreaLabel{
            min-width: 200px;
            max-height: 70px;
            font-size: 160%;
        }

        #textArea{
            min-height: 130px;
            max-height: 130px;
        }

        #formSendButton{
            min-height: 35px;
            font-size: 110%;
        }
    }

    @media(min-width: 1025px) and (max-width: 1328px){

        #mailFormContainer{
            margin-top: 2%;
        }

        .formCell{
            min-height: 40px;
            max-width: 730px;
        }

        .formLabel{
            min-height: 40px;
            max-height: 40px;
            font-size: 160%;
        }

        .formInput{
            min-height: 40px;
            max-height: 40px;
        }

        .input{
            min-height: 30px;
            max-height: 30px;
        }

        #textAreaContainer{
            min-height: 250px;
            max-height: 250px;
            max-width: 730px;
        }

        #textAreaLabel{
            min-width: 200px;
            max-height: 70px;
            font-size: 160%;
        }

        #textArea{
            min-height: 130px;
            max-height: 130px;
        }

        #formSendButton{
            min-height: 35px;
            font-size: 110%;
            margin-top: 2%;
        }
    }

    @media(min-width: 1329px){

#mailFormContainer{
    margin-top: 2%;
}

.formCell{
    min-height: 40px;
    max-height: 42px;
    max-width: 730px;
}

.formLabel{
    min-height: 40px;
    max-height: 40px;
    font-size: 160%;
}

.formInput{
    min-height: 40px;
    max-height: 40px;
}

.input{
    min-height: 30px;
    max-height: 30px;
}

#textAreaContainer{
    min-height: 250px;
    max-height: 250px;
    min-width: 730px;
    max-width: 730px;
}

#textAreaLabel{
    min-width: 200px;
    max-width: 200px;
    min-height: 70px;
    max-height: 70px;
    font-size: 160%;
}

#textArea{
    min-height: 130px;
    max-height: 130px;
}

#formSendButton{
    min-height: 35px;
    max-height: 35px;
    font-size: 110%;
    margin-top: 2%;
}
}
</style>

<script setup>

</script>