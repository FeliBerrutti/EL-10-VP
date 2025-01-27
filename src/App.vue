<template>
  <Menu @changeVisibility="handleVisibilityChange"></Menu>
  <div id="container">
    <div id="box">
        <Transition name="fade">
      <Presentation v-if="visibleComponent === 'presentation'"></Presentation>
        </Transition>
        <Transition name="fade">
      <ContactUs v-if="visibleComponent === 'isContactUsVisible'"
      @changeVisibility="handleVisibilityChange"></ContactUs>
        </Transition>
        <Transition name="fade">
      <FollowUs v-if="visibleComponent === 'isFollowUsVisible'"></FollowUs>
        </Transition>
        <Transition name="fade">
      <MailForm v-if="visibleComponent === 'isContactUsMailVisible'"></MailForm>
        </Transition>
    </div>
  </div>
  <Services ref="auxScroll"></Services>
  <Footer></Footer>
  <WppButton></WppButton>
</template>

<style scoped>
    .fade-enter-active,
    .fade-leave-active{
        transition: opacity 1s ease;
    }

    .fade-enter-from,
    .fade-leave-to{
        opacity: 0;
    }

  #container{
        background-image: url('@/assets/font.jpg');
        background-position: center;
        background-size: cover;
        border-radius: 20px;
        color: white;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    #box{
        border: 2px solid black;
        padding: 0.5%;
        width: 100%;
        top: 0;
        border-radius: 20px;
        overflow: hidden;
        background-color: rgba(10,10,10,0.6);
    }


    @media(max-width: 320px){
        #box{
            min-height: 500px;
            max-height: 580px;
        }
    }

    @media(min-width: 321px) and (max-width: 480px){
        #box{
            min-height: 550px;
            max-height: 700px;
        }
    }

    @media(min-width: 481px) and (max-width: 768px){
        #box{
            min-height: 620px;
            max-height: 620px;
        }
    }

    @media(min-width: 769px) and (max-width: 960px){
        #box{
            min-height: 700px;
            max-height: 740px;
        }
    }

    @media(min-width: 961px) and (max-width: 1024px){
        #box{
            min-height: 700px;
            max-height: 740px;
        }
    }

    @media(min-width: 1025px) and (max-width: 1328px){
        #box{
            min-height: 700px;
            max-height: 740px;
        }
    }

    @media(min-width: 1329px){
      #box{
            min-height: 700px;
            max-height: 740px;
        }
    }
</style>

<script setup>
  import { ref } from 'vue';
  import ContactUs from './components/firstDiv/ContactUs.vue';
  import FollowUs from './components/firstDiv/FollowUs.vue';
  import Presentation from './components/firstDiv/Presentation.vue';
  import Menu from './components/menu/Menu.vue';
  import WppButton from './components/wppButton/WppButton.vue';
  import Services from './components/services/Services.vue';
  import Footer from './components/footer/Footer.vue';
  import MailForm from './components/firstDiv/MailForm.vue';

  const visibleComponent = ref(null);

  function handleVisibilityChange(component){
    visibleComponent.value = component;
  };

  setTimeout(() => {
    visibleComponent.value = 'presentation';
  }, 1000);

</script>