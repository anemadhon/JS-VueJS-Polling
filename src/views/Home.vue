<template>
  <div class="container">
    <section class="vote">
      <h3>Silahkan Nilai Kami</h3>
      <div class="emoticons">
        <Vote />
      </div>
    </section>
    <section class="response">
      <h4>Terima Kasih Atas Penilaian nya</h4>
    </section>
  </div>
</template>

<script>

import Vote from "@/components/Vote.vue";

export default {
  name: "Home",
  components: { Vote }
};

</script>

<style scoped>
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
