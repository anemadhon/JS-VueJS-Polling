<template>
  <div class="container">
    <section class="vote">
      <h3>Silahkan Nilai Kami</h3>
      <div class="emoticons">
        <Vote :whenClick="showResponse"/>
      </div>
    </section>
    <section class="response">
      <transition name="fade">
        <h4 v-if="show">Terima Kasih Atas Penilaian nya</h4>
      </transition>
    </section>
  </div>
</template>

<script>

import Vote from "@/components/Vote.vue";

export default {
  name: "Home",
  data: function(){
    return {
      show: false
    }
  },
  components: { Vote },
  methods: {
    showResponse(){
      this.show = true
    }
  }
};

</script>

<style scoped>
  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }

  .container{
    display: flex;
    flex-wrap: wrap;
    height: 100vh;
    align-items: center;
  }

  section{
    width: 100%;
  }

  .vote {
    height: 50px;
  }

  .emoticons {
    display: flex;
    justify-content: center;
  }
</style>
