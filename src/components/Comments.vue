<template>
  <ul>
    <li v-for="comment in comments" :key="comment">
      {{ comment }}
    </li>
  </ul>
  <input
      @keyup.enter="addComment"
      v-model="newComment"
      placeholder="Add a comment"
  />
</template>

<script>
export default {
  name: "Comments",
  data(){
    return{
      newComment: "",
      comments: [
          'Nice',
          'Bad',
          'Good'
      ]
    }
  },
  methods: {
    addComment() {
      this.comments.push(this.newComment)
      this.newComment = ''
    }


  }
}
</script>

<style scoped>

</style>