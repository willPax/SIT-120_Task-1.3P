<template>
    <div class="main-template">
        <div class="main-section">
            <h1>Previous job history</h1>  
        <table class="table-section" >   
            
            <tr class="header-row">
                <th class="title-col">Position</th>
                <th class="time-col">Duration</th>
                <th class="res-col">Role Responsibilities</th>
            </tr>
            <tr v-for="role in pastJobRoles" :key="title" class="role-row"> 
                <td class="title-col">{{ role.title }}</td>
                <td class="time-col">{{ role.timeFrame }}</td>
                <td class="res-col">
                    <li v-for="pos in role.responsibilities">{{ pos }}</li>
                </td>
            </tr>          
        </table>
    </div>
    </div>
</template>

<script setup>

import { ref } from 'vue'

const pastJobRoles = ref([
    {title: 'Assistant', timeFrame: 'March 2015 - Jan 2017', responsibilities: ['General Assistant', 'Customer Service']},
    {title: 'Another Assistant', timeFrame: 'May 2017 - Jun 2018', responsibilities: ['General Assistant', 'Jnr Team Leader', 'Training']},
    {title: 'Snr Assistant', timeFrame: 'Feb 2018 - July 2020', responsibilities: ['Senior Assistant', 'Team Leader', 'Assistant Manager']},
    {title: 'Jnr Manager', timeFrame: 'March 2020 - Feb 2022', responsibilities: ['Assistant Manager', 'Team Leader', 'Trainee Supervisor']},
    {title: 'Manager', timeFrame: 'Feb 2022 - Current', responsibilities: ['Manager', 'Store Representative',]},
])

</script>

<style scoped>
.table-section {
    table-layout: auto;
    border-collapse: collapse;
    background-color: rgb(220, 231, 232);
    display: flex;
    flex-direction: column;
    width: 100%;
    border-radius: 5px;
}
.main-section h1 {
    margin-left: 5%;
}

.header-row {
  text-align: left; 
  font-size: 15pt;
  padding: 2%;
}
.role-row {
  border-bottom: 1px solid #a3a3a3;
  margin: 1%;
  padding: 1%;
  max-width: 100%;
 }

.role-row:hover {
    background-color: rgb(255, 255, 255);
}

.title-col{
    min-width: 250px;
    max-width: 30%;
}
.time-col{
    min-width: 250px;
    max-width: 30%;
}
.res-col{
    min-width: 40%;
}

table:last-child{
    border-bottom: none;
} 

@media (max-width: 768px) {
    
    .table-section .header-row {
        display: none;
    }

    .table-section h1{
        margin: 2% 15%;
        align-self: center;
    }

    .table-section tr {
        display: block;
        padding: 1%
    }
    .table-section td {
    display: block;
    padding: 1%;
    margin-left: 4%;
    }
}
</style> 