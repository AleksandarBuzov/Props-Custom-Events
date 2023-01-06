<!--UserData.vue-->
<template>
    <section>
      <form @submit.prevent="submitUser">
        <input type="text" placeholder="Your name" v-model="enteredName"/>
        <input type="text" placeholder="Your age" v-model="enteredAge"/>
        <button>Add User</button>
      </form>
    </section>
</template>
<script>
export default {
  emits: ['add-user'],
  data() {
    return {
      enteredName: '',
      enteredAge: '',
    }
  }
  ,
  methods: {
    submitUser() {
      this.$emit('add-user', this.enteredName, this.enteredAge)
    }
  }
}
</script>

