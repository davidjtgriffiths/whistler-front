<template>
<div>
    <!-- Your form goes here -->
    <form @submit.prevent="submitForm">
      <label for="title">Title:</label>
      <input type="text" id="title" v-model="postEmail" />

      <label for="content">Content:</label>
      <textarea id="content" v-model="postPassword"></textarea>

      <button type="submit">Submit</button>
    </form>

    <!-- Display the response -->
    <div v-if="response">
      <h2>Response from Server:</h2>
      <pre>{{ response }}</pre>
    </div>
  </div>
</template>
<script setup>
/* eslint-disable */
import { ref } from 'vue';
import axios from 'axios';

const postEmail = ref('');
const postPassword = ref('');
const response = ref(null);

const submitForm = async () => {
  try {
    const responseData = await axios.post('https://localhost:8000/applogin', {
      "email": postEmail.value,
      "password":postPassword.value,
      "roles": [
        "string",
        "ROLE_USER"
    ],
    "verified": true
    });

    // Handle the response as needed
    response.value = responseData.data;
  } catch (error) {
    // Handle any errors that occurred during the request
    console.error('Error:', error);
  }
};
// const submitForm = async () => {
//   try {
//     const responseData = await axios.post('https://localhost:8000/api/users', {
//       "email": postEmail.value,
//       "roles": [
//         "string",
//         "ROLE_USER"
//     ],
//     "password": "string",
//     "firstName": "string",
//     "lastName": "string",
//     "createdAt": "2023-09-13T09:50:16+01:00",
//     "updatedAt": "2023-09-13T09:50:16+01:00",
//     "userIdentifier": "string",
//     "verified": true
//     });

//     // Handle the response as needed
//     response.value = responseData.data;
//   } catch (error) {
//     // Handle any errors that occurred during the request
//     console.error('Error:', error);
//   }
// };


  const onSubmit = async () => {
    console.log("kjashdjkahs askjdkla")
    const responseData = await axios.post('https://127.0.0.1:8000/api/users', {
    "email": "stringABC",
    "roles": [
        "string",
        "ROLE_USER"
    ],
    "password": "string",
    "firstName": "string",
    "lastName": "string",
    "createdAt": "2023-09-13T09:50:16+01:00",
    "updatedAt": "2023-09-13T09:50:16+01:00",
    "userIdentifier": "string",
    "verified": true
});
  }
</script>
