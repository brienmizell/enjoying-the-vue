<template>
  <div class="container">
    <form v-if="!submitted">
      <div class="row">
        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
          <!-- Exercise 1 -->
          <!-- Create a Signup Form where you retrieve the following Information -->
          <!-- Full Name (First Name + Last Name) -->

          <!-- Exercise 3 -->
          <!-- Edit the Example from above and create a custom "Full Name" Control -->
          <!-- which still holds the First Name and Last Name Input Field -->
          <app-full-name v-model="fullName"></app-full-name>
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
          <button
            type="submit"
            class="btn btn-primary"
            @click.prevent="submitted = true"
          >Submit the Form</button>
        </div>
      </div>
    </form>
    <hr />
    <div class="row" v-if="submitted">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <div class="panel panel-default">
          <div class="panel-heading">
            <h4>Your Data</h4>
          </div>
          <div class="panel-body">
            <p>Full Name: {{fullName}}</p>
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
import FullName from "./components/FullName.vue";
export default {
  data() {
    return {
      fullName: "Brien Mizell",
      email: "",
      password: "",
      storeData: "Yes",
      submitted: false
    };
  },
  components: {
    appFullName: FullName
  }
};
</script>

<style>
</style>
