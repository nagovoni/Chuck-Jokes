<template>
  <div class="text-center pa-4">
    <h1>Search with id: {{ id }}</h1>
    <v-btn @click="back" color="teal-darken-3">Back to home</v-btn>
  </div>

</template>

<script>
  export default {
    data: () => ({
      id: ''
    }),
  beforeMount(){
    console.log(this.$route)
    this.id = this.$route.params.id
  },
  methods: {
    back(){
    this.$router.replace('/home')
  }
  }

  }
</script>
