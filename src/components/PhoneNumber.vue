<script setup>

</script>

<template>
  <div class="phoneContainer">
    <a href="tel:+15864986935"><h1 class="phoneNumber">586-498-6935</h1></a>
    <p>Call today for your free estimate!</p>
  </div>
</template>

<style scoped>

.phoneContainer {
  display: flex;
  flex-direction: column;
  margin-bottom: 20%;
}

.phoneNumber {
  font-size: 8rem;
}

a {
  color: #68bd46;
  text-decoration: none;
}

@media screen and (max-width: 480px) {

  .phoneNumber {
    display: flex;
    justify-content: center;
    font-size: xxx-large;
  }
  .phoneContainer p {
    font-size: x-large;
  }

}
</style>