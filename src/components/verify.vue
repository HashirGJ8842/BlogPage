<template>
    <div>
    <v-row>
      <v-col cols="6" class="mx-auto">
          <v-text-field label="Enter the email" v-model="email" :rules="[rules.email]"></v-text-field>
          <v-text-field label="Enter the password" v-model="password" type="password"></v-text-field>
        <v-btn text v-on:click="check()">Next</v-btn>
      </v-col>
    </v-row>
    </div>
</template>

<script>
  export default {
    name: 'verify',
    data(){
      return{
        email: null,
        password: null,
        rules: {
        email: v => (v || '').match(/@/) || 'Please enter a valid email',
        required: v => !!v || 'This field is required'
      }
      }
    },
    methods:{
      check()
      {
        if(this.email==='hameedhashirniazi@gmail.com'&&this.password==='18723654')
        {
          alert('Welcome')
          this.$emit('isPoster', true);
        }
        else
        {
          alert('wrong')
        }
      }
    }
  }
</script>

<style>

</style>