<template>
   
        <div class="container">
      
      <div class="form-style-6">
        <h1>Simple Form</h1>

        <form @submit.prevent="submitForm"> 
          
          <input v-model="name" type="text" name="name" placeholder="Your Name" required />     
                
          <input v-model="email" type="email" name="email" placeholder="Email Address" required/>
               
        <input type="submit" class="btn btn-primary">
      </form>

      </div>
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
  
        // Submit the form
  
        // Clear the form data and show the thank you message
        this.name = '';
        this.email = '';
        this.submitted = true;
      },
    },
  };
  </script>
  
  <style scoped>
  
  .form-style-6{
	font: 95% Arial, Helvetica, sans-serif;
	max-width: 400px;
	margin: 10px auto;
	padding: 16px;
	background: #F7F7F7;
}

.form-style-6 h1{
	background: #43D1AF;
	padding: 20px 0;
	font-size: 140%;
	font-weight: 300;
	text-align: center;
	color: #fff;
	margin: -16px -16px 16px -16px;
}
.form-style-6 input[type="text"],
.form-style-6 input[type="email"],
.form-style-6 textarea,
.form-style-6 select 
{
	-webkit-transition: all 0.30s ease-in-out;
	-moz-transition: all 0.30s ease-in-out;
	-ms-transition: all 0.30s ease-in-out;
	-o-transition: all 0.30s ease-in-out;
	outline: none;
	box-sizing: border-box;
	-webkit-box-sizing: border-box;
	-moz-box-sizing: border-box;
	width: 100%;
	background: #fff;
	margin-bottom: 4%;
	border: 1px solid #ccc;
	padding: 3%;
	color: #555;
	font: 95% Arial, Helvetica, sans-serif;
}

.form-style-6 input[type="text"]:focus,
.form-style-6 input[type="email"]:focus,
.form-style-6 textarea:focus,
.form-style-6 select:focus
{
	box-shadow: 0 0 5px #43D1AF;
	padding: 3%;
	border: 1px solid #43D1AF;
}

.form-style-6 input[type="submit"],
.form-style-6 input[type="button"]{
	box-sizing: border-box;
	-webkit-box-sizing: border-box;
	-moz-box-sizing: border-box;
	width: 100%;
	padding: 3%;
	background: #43D1AF;
	border-bottom: 2px solid #30C29E;
	border-top-style: none;
	border-right-style: none;
	border-left-style: none;	
	color: #fff;
}
.form-style-6 input[type="submit"]:hover,
.form-style-6 input[type="button"]:hover{
	background: #2EBC99;
} 

  </style>
  