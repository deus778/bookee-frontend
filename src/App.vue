<template>
  <NavigationBar></NavigationBar>
  <GridLayout></GridLayout>
</template>

<script>
import NavigationBar from "@/components/navigation/NavigationBar";
import GridLayout from "@/components/GridPanel/GridLayout";

export default {
  name: 'App',
  components: {
    GridLayout,
    NavigationBar
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
}
</style>
