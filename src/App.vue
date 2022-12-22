<template lang="">
  <main>
    <div class="card">
      <div class="card-img">
        <img
          class="image"
          src="/images/illustration-woman-online-mobile.svg"
          alt="banner"
        />
        <img class="pattern-image" src="/images/bg-pattern-mobile.svg" alt="patten"/>
        <CardText />
      </div>
    </div>
  </main>
</template>
<script>
import CardText from "./components/TextCard.vue";
export default {
  components: {
    CardText,
  },
};
</script>
<style>
main {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.card {
  background-color: white;
  display: flex;
  align-items: center;
  flex-direction: column;
  border-radius: 30px;
  width: 330px;
  margin-top:50px;
}

.image {
  position: absolute;
  width: 200px;
        top: -3%;
        left: 50%; 
        transform: translate(-50%, -50%); 

}
.pattern-image{
  position: relative;
        left: 50%;
        transform: translate(-50%, -50%); 
        top: 45px;
}



</style>
