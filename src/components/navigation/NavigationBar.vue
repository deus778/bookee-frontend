<template>
  <header>
    <nav>
      <ul>
        <li>Test 1</li>
        <li>Test 2</li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "NavigationBar"
}
</script>

<style scoped>

header {
  width: 100%;
  height: 5rem;
  background-color: brown;
}

nav {
  height: 100%;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

li {
  margin: 0 2rem;
}
</style>