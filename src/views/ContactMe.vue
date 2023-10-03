<template>
    <div class="main-template">
        <div class="main-section">
        <span v-if="!sent">
        <span>
        <h1>Thank You for considering me for your position</h1>

        <p>If you are visiting my resume and would like to request my skillset on a project,
        please fill out the following form and I will get back to you</p>
        

        <form class="contact-form">       
        <p>Name<br>
        <input v-model="user_name"> </p>
        <p>Email<br>
        <input v-model="user_email"></p>
        <p>Phone<br>
        <input v-model.number="user_phone"> </p>
        <p>Job Description<br>
        <textarea v-model="user_job" :placeholder="theJob"> enter name</textarea></p>

        <button type="button" class="job-request-btn" @click="send_request">Send!</button>
        </form>
    </span></span>
    <span v-if="sent">
        <h1>Thank You for sending me a thingo, ya champion</h1>
        <p>I will get back to you as soon as possible</p>
    </span>

    </div></div>
</template>

<script setup>

import { ref } from 'vue'

const sent = ref(false)
const user_name = ref('')
const user_email = ref('')
const user_phone = ref(null)
const user_job = ref('')


function send_request(){
    sent.value = true
}

const theJob = ref('Type as much detail about the job as required')

</script>

<style scoped>
.contact-form{
    justify-content: center;
    align-items: center;
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
}
textarea{
    width: 99%;
    height: 250px;
}
input{
    height: 30px;
    width: 99%;
}
.job-request-btn {
  background-color: #e74c3c;
  color: #fff;
  padding: 10px 20px;
  border-radius: 3px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s;
  margin-bottom: 3%;
  width: 100%;
}
 
.job-request-btn:hover {
  background-color: #c0392b;
}
</style>