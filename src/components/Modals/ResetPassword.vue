<template lang="html">
  <!-- Reset password Modal -->
  <div class="modal fade" id="resetPasswordModal" tabindex="-1" role="dialog" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h2 class="modal-title">Zresetuj hasło</h2>
        </div>
        <form method="GET" action="/">
          <div class="modal-body">
            <div class="form-group">
              <label for="resetEmail">Email</label>
              <input id="resetEmail" type="email" name="email" class="form-control" required>
            </div>
            <button type="submit" class="btn btn-primary btn-lg float-right">Zresetuj hasło</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
