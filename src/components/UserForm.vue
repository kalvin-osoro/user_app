<template>
    <div class="user-form">
      <h1>Simple Form</h1>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name:</label>
          <input v-model="name" type="text" id="name" required />
        </div>
        <div class="form-group">
          <label for="email">Email:</label>
          <input v-model="email" type="email" id="email" required />
        </div>
        <button type="submit">Submit</button>
      </form>
      <div v-if="submitted">
        <p>Thank you, {{ submittedName }}!</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        submitted: false,
        submittedName: '',
      };
    },
    methods: {
      submitForm() {
        // Store the name before clearing the form
        this.submittedName = this.name;
  
        // Submit the form (you can send data to a server if needed)
  
        // Clear the form data and show the thank you message
        this.name = '';
        this.email = '';
        this.submitted = true;
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add your responsive styles here */
  </style>
  