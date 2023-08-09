<template>
  <div>
    <v-btn small class="btn text-uppercase rounded-xxl font-weight-bold">
      {{ text }}
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "BTNComponents",
  props:{
    text: {
      type: String,
      require: true,
    }
  }
}
</script>

<style lang="scss" scoped>
.btn{
  font-family: Monospaced;
  background: linear-gradient(90deg, #8176AF 0%, #C0B7E8 100%);
}
</style>
