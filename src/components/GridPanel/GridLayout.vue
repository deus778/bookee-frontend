<template>
  <div class="grid-container">
    <BookEntry v-for="book in books" :key="book.id" :title="book.title" :author="book.author"></BookEntry>
  </div>
</template>

<script>
import BookEntry from "@/components/GridPanel/BookEntry";

export default {
  name: "GridLayout",
  components: {BookEntry},
  data() {
    return {
      books: []
    }
  },
  methods: {
    fetchBooks() {
      fetch('http://localhost:8080/books').then(function (response) {
        if (response.status !== 200) {
          throw response.status;
        } else {
          return response.json();
        }
      }).then((data) => {
        console.log('process data', data);
        for (const id in data) {
          this.books.push({
            title: data[id].title,
            author: data[id].authors[0].firstName + " " + data[id].authors[0].lastName
          })
          console.log(this.books);
        }
      });
    }
  },
  created() {
    this.fetchBooks();
  }
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