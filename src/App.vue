<template>
  <HeaderLogo />
  <HeroSection />
  <DumpsterCalculator />
  <DumpsterPhoneNumber/>
  <JunkRemovalSection/>
  <PhoneNumber />
  <FaqSection />
  <SocialLinkBar />
</template>

<script>
import DumpsterCalculator from "@/components/DumpsterCalculator.vue";
import HeroSection from "@/components/HeroSection.vue";
import FaqSection from "@/components/FaqSection.vue";
import HeaderLogo from "@/components/HeaderLogo.vue";
import SocialLinkBar from "@/components/SocialLinkBar.vue";
import PhoneNumber from "@/components/PhoneNumber.vue";
import DumpsterPhoneNumber from "@/components/DumpsterPhoneNumber.vue";
import JunkRemovalSection from "@/components/JunkRemovalSection.vue";


export default {
  name: 'App',
  components: {
    JunkRemovalSection,
    DumpsterPhoneNumber,
    PhoneNumber,
    HeaderLogo,
    HeroSection,
    DumpsterCalculator,
    FaqSection,
    SocialLinkBar,
  }
}


</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #eb1c25;
  font-family: "Stencil";
  padding-top: 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 0;
  background-color: rgba(0, 0, 0, 0.72);


}

#landingLogo {
  display: flex;
  max-width: 35%;
  max-height: 35%;
}

p {
  font-size: xx-large;
  font-weight: bold;


}



</style>
