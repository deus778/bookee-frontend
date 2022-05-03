<template>
  <div @mouseover="setHoveringFlag(true)" @mouseleave="setHoveringFlag(false)">
    <p :class="{entryHovered: isHovered}"> {{ title }}</p>
  </div>
</template>

<script>
export default {
  name: "BookEntry",
  props: {
    title: {
      type: String,
      required: true
    },
  },
  data() {
    return {
      isHovered: false
    }
  },
  watch: {
    isHovered() {
      return this.isHovered
    }
  },
  methods: {
    setHoveringFlag(hovered) {
      this.isHovered = hovered
    }
  }
}
</script>

<style scoped>

div {
  background-color: antiquewhite;
  height: 5rem;
  width: 10rem;
  margin: 0.5em 0.5em 0.5em 0.5em;
  display: flex;
  justify-content: center;
  align-items: center;
}

.entryHovered {
  color: blue;
}

</style>