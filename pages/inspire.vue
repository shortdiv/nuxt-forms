<template>
  <v-layout>
    <v-flex text-xs-center>
      <v-form ref="form" name="contact" method="POST" data-netlify="true">
        <input type="hidden" name="contact" value="contact-form">
        <v-text-field
          v-model="name"
          name="name"
          label="Your Name"
          type="text"
        />
        <v-text-field
          v-model="email"
          name="email"
          label="Your Email"
          type="email"
        />
        <v-select
          :items="items"
          name="role"
          label="Your Role"
        />
        <v-text-field
          v-model="message"
          name="message"
          label="message"
        />
        <v-btn type="submit">
          submit
        </v-btn>
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
