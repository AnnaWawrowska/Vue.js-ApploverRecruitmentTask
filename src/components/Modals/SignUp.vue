<template lang="html">
	<!-- Sign Up Modal -->
	<div class="modal fade" id="signUpModal" tabindex="-1" role="dialog" aria-hidden="true">
		<div class="modal-dialog modal-dialog-centered" role="document">
			<div class="modal-content">
				<div class="modal-header">
					<h2 class="modal-title">Załóż konto</h2>
				</div>
				<form id="formSignUp" @submit.prevent="signUp">
					<div class="modal-body">
						<div class="form-group">
							<label for="signUpEmail">Email</label>
							<input v-model="email" id="signUpEmail" type="email" name="email" class="form-control" required>
						</div>
						<div class="form-group">
							<label for="signUpPassword">Hasło</label>
							<input v-model="password" id="signUpPassword" type="password" name="password" class="form-control" required>
						</div>
						<button type="submit" class="btn btn-primary btn-lg float-right">Załóż konto</button>
					</div>
				</form>
				<div class="modal-footer">
					<p>*Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae placeat nemo excepturi officia eligendi! Fugit, illo iure eius perspiciatis quidem!</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from 'axios';

export default {
	data() {
		return {
			email: '',
			password: ''
		}
	},
	methods: {
		signUp() {
			const authData = {
				email: this.email,
				password: this.password
			};
			axios.post('https://foodsi-stage.applover.pl/api/v1/auth', authData)
			.then(function (response) {
				console.log(response);
			})
			.catch(function (error) {
				console.log(error);
			});
		}
	}
}
</script>
