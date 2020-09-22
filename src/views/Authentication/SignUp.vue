<template>
   <v-row >
    <v-col cols="3"></v-col>
      <v-col cols="6">
        <v-card class="pa-2" outlined tile>
          <v-form ref="form" v-model="valid" lazy-validation >
              <v-text-field v-model="name" :counter="10" :rules="nameRules" label="Name"  required > </v-text-field>

              <v-text-field v-model="email" :rules="emailRules" label="E-mail"  required></v-text-field>

              <v-select v-model="select" :items="items" :rules="[v => !!v || 'Item is required']" label="Item" required></v-select>

              <v-checkbox v-model="checkbox" :rules="[v => !!v || 'You must agree to continue!']"
                 label="Do you agree?"  required
              ></v-checkbox>

              <v-row>
                 <v-spacer></v-spacer>
                  <v-btn
                    color="success"
                    class="mr-4"
                    @click="reset"
                  >
                    Register
                  </v-btn>

                  <v-btn
                    color="warning"
                    @click="resetValidation"
                  >
                  Clear
                  </v-btn>

               <v-spacer></v-spacer>
              </v-row>
            </v-form>
        </v-card>
      </v-col>
      <v-col cols="3"></v-col>
</v-row>
</template>

<script>
  import { validationMixin } from 'vuelidate'
  import { required, maxLength, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
      name: { required, maxLength: maxLength(10) },
      email: { required, email },
      select: { required },
      checkbox: {
        checked (val) {
          return val
        },
      },
    },

    data: () => ({
      name: '',
      email: '',
      select: null,
      items: [
        'Item 1',
        'Item 2',
        'Item 3',
        'Item 4',
      ],
      checkbox: false,
    }),

    computed: {
      checkboxErrors () {
        const errors = []
        if (!this.$v.checkbox.$dirty) return errors
        !this.$v.checkbox.checked && errors.push('You must agree to continue!')
        return errors
      },
      selectErrors () {
        const errors = []
        if (!this.$v.select.$dirty) return errors
        !this.$v.select.required && errors.push('Item is required')
        return errors
      },
      nameErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.maxLength && errors.push('Name must be at most 10 characters long')
        !this.$v.name.required && errors.push('Name is required.')
        return errors
      },
      emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('Must be valid e-mail')
        !this.$v.email.required && errors.push('E-mail is required')
        return errors
      },
    },

    methods: {
      submit () {
        this.$v.$touch()
      },
      clear () {
        this.$v.$reset()
        this.name = ''
        this.email = ''
        this.select = null
        this.checkbox = false
      },
    },
  }
</script>
