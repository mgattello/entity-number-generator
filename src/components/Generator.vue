<template>
    <div class="container">
      <div class="container-entity">
        <span class="entity-number">{{ generateEntityNumber }}</span>
      </div>

      <div calss="container-input">
        <input class="user-input" type="text" v-model="msg" maxlength="1" />
      </div>
    </div>
</template>

<script>
export default {
  name: 'Generator',
  data: function () {
    return { 
      msg: ''
    }
  },
  computed: {
    generateEntityNumber: function() {
      const unicode = this.msg.charCodeAt(0)
      return `&#${unicode};`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
    .container
      display: inline

      .container-entity
        min-height: 15rem

        .entity-number 
          min-height: 15rem
          height: 20rem
          font-size: 10rem
          color: rgb(random(255), random(255), random(255))

</style>
