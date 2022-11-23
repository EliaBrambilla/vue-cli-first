<template>
  <div>
    <div class="red" @click="saluta">
      
      <div class="inner">Sono Elia</div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'FirstComponent',
  data() {
    return {
      text: '',
    };
  },
  methods: {
    saluta() {
      console.log('ti saluta il tuo primo componente');
    },
  },
};
</script>

<style lang="scss" scoped>
$bgColor: red;
@mixin ac-square {
    width: 150px;
    height: 150px;
}
.red-square{
    @include ac-square();
    background-color: brown;
}
/*
.red {
   background-color: $bgColor;
    .inner{
        background-color: yellowgreen;
    }
    &.active{
        background-color: blue;
    }
}
.inner{
    background-color: yellow;
}
*/
// il preprocessore trasforma il scss in css standard:
.red {
    background-color: red;
}
.red .inner{
    background-color: yellowgreen;
}
.red.active{
    background-color: blue;
}
.inner{
     background-color: yellow;
}
</style>