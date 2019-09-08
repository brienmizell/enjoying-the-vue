<template>
  <div class="container">
    <form>
      <div class="row">
        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
          <!-- Exercise 1 -->
          <!-- Create a Signup Form where you retrieve the following Information -->
          <!-- Full Name (First Name + Last Name) -->
          <div class="form-group">
            <label for="firstName">First Name:</label>
            <input type="text" id="firstName" class="form-control" v-model.lazy="firstName" />
            <label for="lastName">Last Name:</label>
            <input type="text" id="lastName" class="form-control" v-model.lazy="lastName" />
          </div>
          <!-- Mail -->
          <div class="form-group">
            <label for="email">Email:</label>
            <input type="text" name id="email" class="form-control" v-model.lazy="email" />
          </div>
          <!-- Password -->
          <div class="form-group">
            <label for="password">Password:</label>
            <input type="password" name="password" id class="form-control" v-model="password" />
          </div>
          <!-- Store Data? Yes/No -->
          <div class="form-check">
            Store Data?
            <br />
            <label for>
              <input type="radio" value="Yes" v-model="storeData" /> Yes
            </label>
            <label for>
              <input type="radio" value="No" v-model="storeData" /> No
            </label>
          </div>
          <!-- Exercise 2 -->
          <!-- Only display the Form if it has NOT been submitted -->
          <!-- Display the Data Summary ONCE the Form HAS been submitted -->

          <!-- Exercise 3 -->
          <!-- Edit the Example from above and create a custom "Full Name" Control -->
          <!-- which still holds the First Name and Last Name Input Field -->
        </div>
      </div>
    </form>
    <hr />
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <div class="panel panel-default">
          <div class="panel-heading">
            <h4>Your Data</h4>
          </div>
          <div class="panel-body">
            <p>Full Name: {{firstName }} {{ lastName}}</p>
            <p>Email: {{email}}</p>
            <p>Password: {{password}}</p>
            <p>Store in Database?: {{storeData}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      firstName: "",
      lastName: "",
      password: "",
      storeData: true
    };
  }
};
</script>

<style>
</style>
