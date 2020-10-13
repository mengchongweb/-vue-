<template>
  <li class="item" @click='handleDelete'>{{content}}</li>
</template>

<script>
export default {
  name: 'TodoItem',
  props: ['content', 'index'],
  data () {
    return {

    }
  },
  methods: {
    handleDelete () {
      this.$emit('delete', this.index)
    }
  }
}
</script>
<!-- 加scoped -->
<style scoped>
  .item{
    color:red;
  }

</style>
