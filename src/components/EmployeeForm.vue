.<template>
  <div class="employes-form">
    <form>
      <label for>Employee Name</label>
      <input type="text /" />
      <label for>Employee Email</label>
      <input type="text /" />
      <button>Add Employee</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "employee-form",
  data() {
    return {
      employee: {
        name: "",
        email: ""
      }
    };
  }
};
</script>

<style scoped>
form {
  margin-bottom: 2rem;
}
input {
  width: 100%;
}
button{ 
  margin-top: 1rem;
}
</style>