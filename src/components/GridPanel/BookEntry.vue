<template>
  <div :class="{entryHovered: isHovered}" @mouseover="setHoveringFlag(true)" @mouseleave="setHoveringFlag(false)">
    <div>
      <b>{{ title }}</b>
      <div class="imageContainer">
        <img src="../../assets/book.png">
      </div>
      <p>by {{ author }}</p>
    </div>
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
    author: {
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
  height: 20rem;
  width: 20rem;
  margin: 0.5em 0.5em 0.5em 0.5em;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: column;
  border-radius: 5em;
}

.entryHovered {
  color: blue;
  flex-grow: 3;
}

.imageContainer {
  width: 6em;
  height: 6em;
}

.imageContainer img {
  width: 100%;
  height: 100%;
}

</style>