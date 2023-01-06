<template>
<section>
  <h2>Kole poluchi li</h2>
  <user-data @add-user="addUser"></user-data>
  <active-user
:username="user.name" :userage="user.age"
  ></active-user>
</section>
</template>

<script>
export  default{
  data(){
    return {
      user: {
        name: 'kole',
        age: 30
      }
    }
  },
  methods: {
    addUser(name, age){
      const addedUser = {
        name: name,
        age: +age,
      }
      this.user = addedUser
    }
  }
}
</script>

<style>
html {
  font-family: sans-serif;
}
section{
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid #ccc;
  padding: 1rem
}
</style>