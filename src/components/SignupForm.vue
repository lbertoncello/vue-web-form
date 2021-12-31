<template>
  <form>
    <label>Email: </label>
    <!-- 
      v-model creates a two-way data binding between the input field and the given data attribute.
      It means that whatever change made by the user on the input field will be reflected in the component's data attribute,
      and whatever change made on the component's data attribute will be reflected in the input field.
    -->
    <input type="email" required v-model="email">

    <label>Password: </label>
    <input type="password" required v-model="password">

    <label>Role:</label>
    <select v-model="role">
      <option value="developer">Web Developer</option>
      <option value="designer">Web Designer</option>
    </select>

    <!-- Way to work with a single checkbox -->
    <div class="terms">
      <input type="checkbox" v-model="terms" required>
      <label>Accept terms and conditions</label>
    </div>

    <!-- Way to work with multiple (a group of) checkboxes -->
    <!-- <div>
      <input type="checkbox" value="shaun" v-model="names">
      <label>Shaun</label>
    </div>
    <div>
      <input type="checkbox" value="yoshi" v-model="names">
      <label>Yoshi</label>
    </div>
    <div>
      <input type="checkbox" value="mario" v-model="names">
      <label>Mario</label>
    </div> -->

  </form>

  <p>Email: {{ email }}</p>
  <p>Password: {{ password }}</p>
  <p>Role: {{ role }}</p>
  <p>Terms accepted: {{ terms }}</p>
  <p>Names: {{ names }}</p>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: '',
      role: 'designer',
      terms: false,
      // names: []
    }
  }
}
</script>

<style>
  form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
  }
  label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555
  }
  input[type="checkbox"] {
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 2px;
  }
</style>