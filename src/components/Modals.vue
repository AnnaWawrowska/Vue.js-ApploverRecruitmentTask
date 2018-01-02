<template lang="html">
  <div>
    <login></login>
    <signUp></signUp>
    <resetPassword></resetPassword>
  </div>
</template>

<script>
import Login from './Modals/Modal-login.vue';
import SignUp from './Modals/Modal-signUp.vue';
import ResetPassword from './Modals/Modal-resetPassword.vue';


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
