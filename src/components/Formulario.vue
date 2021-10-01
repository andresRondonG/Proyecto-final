<template>
  <div>
    <h1>Ingrese los siguientes datos</h1>
    <br>
    <br>
    
    <form id="form">
      <v-text-field
        v-model="name"
        :error-messages="nameErrors"
        :counter="10"
        label="Name"
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
      ></v-text-field>
      <v-text-field
        v-model="last_name"
        :error-messages="nameErrors"
        :counter="10"
        label="Last name"
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
      ></v-text-field>
      <v-text-field
        v-model="phone"
        :error-messages="phoneErrors"
        :counter="15"
        label="phone"
        required
        @input="$v.phone.$touch()"
        @blur="$v.phone.$touch()"
      ></v-text-field>
      <v-text-field
        v-model="email"
        :error-messages="emailErrors"
        label="E-mail"
        required
        @input="$v.email.$touch()"
        @blur="$v.email.$touch()"
      ></v-text-field>
      <v-select
        v-model="select"
        :items="rh"
        :error-messages="selectErrors"
        label="RH"
        required
        @change="$v.select.$touch()"
        @blur="$v.select.$touch()"
      ></v-select>
       <v-text-field
        v-model="blood_type"
        :error-messages="BloodTypeErrors"
        :counter="15"
        label="Blood type"
        required
        @input="$v.rh.$touch()"
        @blur="$v.rh.$touch()"
      ></v-text-field>
      <v-checkbox
        v-model="checkbox"
        :error-messages="checkboxErrors"
        label="Do you agree?"
        required
        @change="$v.checkbox.$touch()"
        @blur="$v.checkbox.$touch()"
      ></v-checkbox>

      <v-btn class="mr-4" @click="principal"> to register </v-btn>
      <v-btn @click="clear"> Cancel </v-btn>
    </form>
  </div>
</template>

<script>
export default {
  data: () => {
    return {};
  },

  methods: {
      principal(){
          this.$router.push('/home')
      }
  },

  created: () => {},

  computed: {},
};
</script>

<style>
#form{
    padding-left: 30%;
    padding-right: 30%;
    padding-bottom: 10%;
}
h1{
    text-align: center;
    padding-top: 5%;
}
</style>