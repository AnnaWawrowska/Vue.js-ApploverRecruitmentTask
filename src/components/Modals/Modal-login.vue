<template lang="html">
  <!--Login Modal -->
  <div class="modal fade" id="loginModal" tabindex="-1" role="dialog" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h2 class="modal-title">Logowanie</h2>
        </div>
        <form method="GET" action="/">
          <div class="modal-body">
            <div class="form-group">
              <label for="loginEmail">Email</label>
              <input id="loginEmail" type="email" name="email" class="form-control" required>
            </div>
            <div class="form-group">
              <label for="loginPassword">Hasło</label>
              <input id="loginPassword" type="password" name="password" class="form-control" required >
            </div>
          </div>
          <div class="modal-footer">
            <button type="submit" class="btn btn-primary btn-block">Zaloguj</button>
            <span class="modal-spacer">lub</span>
            <button type="button" class="btn btn-primary btn-block">Zaloguj się przez Facebook</button>
            <button type="button" class="btn btn-primary btn-block">Zaloguj się przez Linkedln</button>
            <button type="button" class="btn btn-secondary btn-block" data-toggle="modal" data-target="#resetPasswordModal" data-dismiss="modal">Zresetuj hasło</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
