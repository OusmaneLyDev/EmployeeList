<template>
    <div class="employee-list">
      <ol>
        <li v-for="employee in employees" :key="employee.id" class="employee-item">
          {{ employee.name }}
        </li>
      </ol>
    </div>
  </template>
  
  <script>
  export default {
    name: 'EmployeeList',
    data() {
      return {
        employees: [
          { id: 1, name: 'Ly Ousmane' },
          { id: 2, name: 'Traoré Harouna' },
          { id: 3, name: 'Seme Thiello' },
          { id: 4, name: 'Ba Zakaria' }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .employee-list {
    max-width: 500px;
    margin: auto;
    padding: 30px;
    font-family: Arial, sans-serif;
  }
  
  .employee-list ol {
    align-items: center;
    list-style-type: decimal;
    padding-left: 20px;
    cursor: pointer;
  }
  
  .employee-item {
    color: rgb(255, 255, 255);
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    margin-bottom: 10px;
    transition: background-color 0.3s ease;
  }
  
  .employee-item:hover {
    background-color: #35c53ab6;
  }
  </style>
  