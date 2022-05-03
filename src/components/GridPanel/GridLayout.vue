<template>
  <div class="grid-container">
    <BookEntry v-for="book in books" :key="book.id" :title="book.name"></BookEntry>
  </div>
</template>

<script>
import BookEntry from "@/components/GridPanel/BookEntry";

export default {
  name: "GridLayout",
  components: {BookEntry},
  data() {
    return {
      books: [
        {
          id: 1,
          name: "Hergergerth"
        },
        {
          id: 2,
          name: "Hergergerth"
        },
        {
          id: 3,
          name: "Hergergerth"
        },
        {
          id: 4,
          name: "Hergergerth"
        },
        {
          id: 5,
          name: "Hergergerth"
        },
        {
          id: 6,
          name: "Hergergerth"
        },
        {
          id: 7,
          name: "Hergergerth"
        },
        {
          id: 8,
          name: "Hergergerth"
        },
        {
          id: 9,
          name: "Hergergerth"
        },
        {
          id: 10,
          name: "Hergergerth"
        },
        {
          id: 11,
          name: "Hergergerth"
        },
        {
          id: 12,
          name: "Hergergerth"
        },
        {
          id: 13,
          name: "Hergergerth"
        },
        {
          id: 14,
          name: "Hergergerth"
        },
        {
          id: 15,
          name: "Hergergerth"
        },
        {
          id: 16,
          name: "Hergergerth"
        },

      ]
    }
  },
}
</script>

<style scoped>

.grid-container {
  display: flex;
  background-color: azure;
  justify-content: flex-start;
  flex-flow: row wrap; /*short for flex-wrap and flex-direction*/
}

</style>