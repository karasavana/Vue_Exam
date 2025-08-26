<template>
  <p>Hello, {{ username }}</p>
</template>

<script>
export default {
  name: "Greeting",
  props: {
    username: {
      type: String,
      required: true
    }
  }
}
</script>
