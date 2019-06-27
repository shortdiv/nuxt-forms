<template>
  <v-layout>
    <v-flex text-xs-center>
      <v-form ref="form" name="contact" method="POST" data-netlify="true">
        <input type="hidden" name="contact" value="contact-form">
        <label for="name">Your Name:</label>
        <input type="text" name="name" v-model="name">
        <label for="name">Your Email:</label>
        <input type="email" name="email" v-model="email">
        <label for="role">Your Role</label>
        <select name="role" id="">
          <option value="leader">Leader</option>
          <option value="follower">Follower</option>
        </select>
        <label for="message">Message:</label>
        <input type="text" name="message" v-model="message">
        <button type="submit" class="v-btn theme--dark">
          Submit
        </button>
      </v-form>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      name: null,
      email: null,
      message: null,
      items: ['Leader', 'Follower']
    }
  }
}
</script>
