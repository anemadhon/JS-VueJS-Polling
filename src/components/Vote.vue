<template>
  <div class="container-emot">
    <button v-for="(emot, index) in emoticons"
            :key="index"
            :id="emot"
            :value="emot"
            @click="forVote"
            class="emot-btn"
        ></button>
  </div>
</template>

<script>

export default {
    name: "Home",
    components: {},
    data: function () {
        return {
            emoticons: ['very-bad','bad','ok','good','very-good']
        }
    },
    methods: {
        forVote(e){
            let voted = e.target.value;
            localStorage.setItem('vote', voted)
        }
    }
};

</script>

<style scoped>
  .container-emot {
    display: flex;
  }

  .emot-btn {
    background: url('~@/assets/emoticon.png');
    width: 101px;
    height: 100px;
    outline: none;
    border: none;
    margin: 50px 10px;
    cursor: pointer;
  }

  .emoticons {
    display: flex;
    justify-content: center;
  }

  #very-bad {
    background-position: 0px 0px;
  }
  
  #very-bad:hover {
    background-position: 0px -100px;
  }
  
  #very-bad:active {
    background-position: 0px -200px;
  }
  
  #bad {
    background-position: -101px 0px;
  }
  
  #bad:hover {
    background-position: -101px -100px;
  }
  
  #bad:active {
    background-position: -101px -200px;
  }
  
  #ok {
    background-position: -202px 0px;
  }
  
  #ok:hover {
    background-position: -202px -100px;
  }
  
  #ok:active {
    background-position: -202px -200px;
  }
  
  #good {
    background-position: -303px 0px;
  }
  
  #good:hover {
    background-position: -303px -100px;
  }
  
  #good:active {
    background-position: -303px -200px;
  }
  
  #very-good {
    background-position: -404px 0px;
  }
  
  #very-good:hover {
    background-position: -404px -100px;
  }
  
  #very-good:active {
    background-position: -404px -200px;
  }
</style>
