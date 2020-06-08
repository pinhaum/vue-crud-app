<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>

    <employee-form @add:employee="addEmployee"/>
    <employee-table :employees="employees" />
  </div>
</template>

<script>
  import EmployeeTable from '@/components/EmployeeTable.vue'
  import EmployeeForm from '@/components/EmployeeForm.vue'

export default {
  name: 'app',
  components: {
    EmployeeTable,
    EmployeeForm
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: 'Gato Felix',
          email: 'lechat@felix.com',
        },
        {
          id: 2,
          name: 'Hatori Hanzo',
          email: 'ginsu2000@hatori.com',
        },
        {
          id: 3,
          name: 'Ítalo Americano',
          email: 'italy@america.com',
        },
      ],
    }
  },
  methods: {
    addEmployee(employee) {
      const lastId = 
        this.employees.length > 0 
          ? this.employees[this.employees.length -1].id 
          : 0;

      const id = lastId + 1;
      const newEmployee = { ...employee, id };

      this.employees = [...this.employees, newEmployee]
    }
  }
}
</script>

<style>

button{
  background: #009435;
  border: 1px solid #009435
}

.small-container {
  max-width: 680px;
}
</style>
