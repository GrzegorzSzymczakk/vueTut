<template>
  <div id="api">
    <div class="contain">
      <h2>Blog post</h2>
      <form @submit-prevent="addPost">
        <input v-model="newTitle" placeholder="title" required>
        <input v-model="newAuthor" placeholder="author" required>
        <select v-model="newLabel" required>
          <option disabled value="">Add a new label</option>
          <option v-for="category in categories"
                  :value="category"> {{ category }}
          </option>
        </select>
        <button type="submit">Add New Blog Post</button>
      </form>
    </div>

    <select v-model="selected">
      <option disabled value="">Filter with a label</option>
      <option v-for="category in categories"
              :value="category">{{ category }}

      </option>
    </select>

    <div v-for="post in filteredByLabel"
         :key="post.title" class="post">
      <span class="label">{{ post.label }}</span>
      <p>{{ post.title }}</p>
      <small>{{ post.author }}</small>
    </div>
  </div>
</template>

<script>
export default {
  name: "CompProperties",
  data() {
    return {
      selected: '',
      categories: ['science', 'math', 'poetry', 'history'],
      posts: [
        {
          author: '@Gogo the great',
          title: 'Undefeated',
          label: 'science'
        },
        {
          author: '@Soso',
          title: 'Tututu',
          label: 'math'
        }
      ],
      newTitle: '',
      newAuthor: '',
      newLabel: ''
    }
  },
  methods: {
    addPost() {
      let addedPost = {
        author: this.newAuthor,
        title: this.newTitle,
        label: this.newLabel
      }
      this.posts.push(addedPost)
      this.newTitle = '';
      this.newAuthor = '';
      this.newLabel = '';
    }

  },
  computed: {
    filteredByLabel() {
      let filter = new RegExp(this.selected, 'i');
      return this.posts.filter(el => el.label.match(filter))
    }
  }
}
</script>

<style scoped>

</style>