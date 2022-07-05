<template>
  <b-container>
    <h1 class="mt-5 mb-4">Profile:</h1>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">Prénom</th>
          <th scope="col">Nom</th>
          <th scope="col">Email</th>
          <th scope="col">Adresse</th>
          <th scope="col">Téléphone</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>{{ getUser.lastName }}</td>
          <td>{{ getUser.firstName }}</td>
          <td>{{ getUser.email }}</td>
          <td>{{ getUser.address }}</td>
          <td>{{ getUser.phone }}</td>
        </tr>
      </tbody>
    </table>
  </b-container>
</template>

<script>
import { mapGetters } from "vuex";
import auth from "@/middlewares/auth";
export default {
  middleware: [auth],
  layout: "loggedIn",
  computed: {
    ...mapGetters("auth", ["getUser"]),
    userFullName() {
      return `${this.getUser}`;
    }
  }
};
</script>
