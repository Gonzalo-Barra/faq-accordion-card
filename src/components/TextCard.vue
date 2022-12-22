<template lang="">
  <div class="text">
    <h1 class="">FAQ</h1>
    <div class="card-text">
      <h2 :style="{ fontWeight: isBold ? '700' : 'normal' }">
        How many team members can I invite?
      </h2>

      <img
        @click.native="rotateImage"
        @click="toggleDiv"
        src="/images/icon-arrow-down.svg"
        :style="{ transform: `rotate(${angle}deg)` }"
        alt="arrow down"
      />
    </div>
    <p v-if="showDiv">
      You can invite up to 2 additional users on the Free plan. There is no
      limit on team members for the Premium plan.
    </p>
    <hr />
    <div class="card-text">
      <h2 :style="{ fontWeight: isBold2 ? '700' : 'normal' }">
        What is the maximum file upload size?
      </h2>
      <img
        @click.native="rotateImage2"
        @click="toggleDiv2"
        :style="{ transform: `rotate(${angle2}deg)` }"
        src="/images/icon-arrow-down.svg"
        alt="arrow down"
      />
    </div>
    <p v-if="showDiv2">
      No more than 2GB. All files in your account must fit your allotted storage
      space.
    </p>
    <hr />
    <div class="card-text">
      <h2 :style="{ fontWeight: isBold3 ? '700' : '500' }">
        How do I reset my password?
      </h2>
      <img
        @click.native="rotateImage3"
        @click="toggleDiv3"
        :style="{ transform: `rotate(${angle3}deg)` }"
        src="/images/icon-arrow-down.svg"
        alt="arrow down"
      />
    </div>
    <p v-if="showDiv3">
      Click “Forgot password” from the login page or “Change password” from your
      profile page. A reset link will be emailed to you.
    </p>
    <hr />
    <div class="card-text">
      <h2 :style="{ fontWeight: isBold4 ? '700' : 'normal' }">
        Can I cancel my subscription?
      </h2>
      <img
        @click.native="rotateImage4"
        @click="toggleDiv4"
        :style="{ transform: `rotate(${angle4}deg)` }"
        src="/images/icon-arrow-down.svg"
        alt="arrow down"
      />
    </div>
    <p v-if="showDiv4">
      Yes! Send us a message and we’ll process your request no questions asked.
    </p>
    <hr />
    <div class="card-text">
      <h2 :style="{ fontWeight: isBold5 ? '700' : 'normal' }">
        Do you provide additional support?
      </h2>
      <img
        @click.native="rotateImage5"
        @click="toggleDiv5"
        :style="{ transform: `rotate(${angle5}deg)` }"
        src="/images/icon-arrow-down.svg"
        alt="arrow down"
      />
    </div>

    <p v-if="showDiv5">
      Chat and email support is available 24/7. Phone lines are open during
      normal business hours.
    </p>
    <hr />
  </div>
</template>
<script>
export default {
  data() {
    return {
      isBold: false,
      isBold2: false,
      isBold3: false,
      isBold4: false,
      isBold5: false,
      angle: 0,
      angle2: 0,
      angle3: 0,
      angle4: 0,
      angle5: 0,
      showDiv: false,
      showDiv2: false,
      showDiv3: false,
      showDiv4: false,
      showDiv5: false,
    };
  },
  methods: {
    toggleDiv() {
      this.showDiv = !this.showDiv;
      this.isBold = !this.isBold;
    },
    toggleDiv2() {
      this.showDiv2 = !this.showDiv2;
      this.isBold2 = !this.isBold2;
    },
    toggleDiv3() {
      this.showDiv3 = !this.showDiv3;
      this.isBold3 = !this.isBold3;
    },
    toggleDiv4() {
      this.showDiv4 = !this.showDiv4;
      this.isBold4 = !this.isBold4;
    },
    toggleDiv5() {
      this.showDiv5 = !this.showDiv5;
      this.isBold5 = !this.isBold5;
    },
    rotateImage() {
      this.angle = this.angle === 0 ? 180 : 0;
    },
    rotateImage2() {
      this.angle2 = this.angle2 === 0 ? 180 : 0;
    },
    rotateImage3() {
      this.angle3 = this.angle3 === 0 ? 180 : 0;
    },
    rotateImage4() {
      this.angle4 = this.angle4 === 0 ? 180 : 0;
    },
    rotateImage5() {
      this.angle5 = this.angle5 === 0 ? 180 : 0;
    },
  },
};
</script>
<style>

h1 {
  text-align: center;
  font-family: "Kumbh Sans", sans-serif;
  font-weight: 700;
  margin-bottom: 30px;
}

h2,
p {
  text-align: center;
  font-family: "Kumbh Sans", sans-serif;
  font-weight: 500;
  font-size: 13px;
 
}

hr {
  opacity: 10%;
  margin: 0 20px;
  
}

.card-text {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 10px 20px;

}

.text {
  padding-bottom: 40px;
  margin-top: 0;
  margin: 0 0px;
  width: 300px;
}
.text p {
  text-align: justify;
  margin: 10px 20px;
  padding-bottom: 10px;
  padding-right: 30px;
}

</style>
