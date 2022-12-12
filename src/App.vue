<template>
  <v-app>
    <v-card width="400" class="mx-auto mt-5">
      <v-card-title>
        <h1 class="display-1">Acceder</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field label="Username" prepend-icon="mdi-account-circle" />
          <v-text-field :type="showPassword ? 'text' : 'password'" label="Password" prepend-icon="mdi-lock" :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'" @click:append="showPassword = !showPassword"/>
        </v-form>
        <!-- Cuando clickas en el botón se activa y se puede leer la contraseña -->
      </v-card-text>
      <v-card-actions>
        <v-btn color="success">Registro</v-btn>
        <v-spacer></v-spacer>
        <v-btn color="info">Acceder</v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
export default {
  name: "App",
components: {

},
  data: () => ({
showPassword:false
  }),
};
</script>
