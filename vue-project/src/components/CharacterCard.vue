<script>
export default {
  data() {
    return {
      userList: []
    }
  },
  methods: {
    addNewUser() {
      this.userList.push(this.newUser);
      this.newUser = {name: ""};
    },
    favoriteUser(userName) {
      this.favoriteUser.push(userName)
    }
  }
}
</script>

<template>
  <div>
    <p>{{user.name}}</p>
    <button @click="favoriteCharacter(character)">Favorite</button>
  </div>
</template>