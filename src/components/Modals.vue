<template lang="html">
  <div>
    <login></login>
    <signUp></signUp>
    <resetPassword></resetPassword>
  </div>
</template>

<script>
import Login from './Modals/Login.vue';
import SignUp from './Modals/SignUp.vue';
import ResetPassword from './Modals/ResetPassword.vue';


export default {
  data () {
    return {
    }
  },
  components: {
    'login': Login,
    'signUp': SignUp,
    'resetPassword': ResetPassword,
  },
}
</script>
