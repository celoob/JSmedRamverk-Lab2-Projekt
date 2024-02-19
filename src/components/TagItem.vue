<template>
  <h6 @click="handleClick" class="tag-item">{{ tag }}</h6>
</template>

<script>
export default {
  props: {
    tag: {
      type: String,
      required: true
    }
  },
  methods: {
    handleClick() {
      this.$emit('tag-clicked', this.tag)
    }
  }
}
</script>

<style></style>
