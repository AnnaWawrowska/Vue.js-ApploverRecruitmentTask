<template lang="html">
  <header class="header">
    <div class="container">
      <div class="row">
        <div class="col">
          <ul class="nav justify-content-end">
            <li class="nav-item">
              <button class="nav-link" data-toggle="modal" data-target="#signUpModal">załóż konto</button>
            </li>
            <li class="nav-item">
              <button type="button" class="nav-link nav-link--green" data-toggle="modal" data-target="#loginModal">zaloguj</button>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@import '../styles/helpers/colors.scss';
@import '../styles/helpers/include-media.scss';

.header {
  background-color: $color--marine-blue;
  height: 50px;
}

.nav {
  padding-top: 17px;
  margin: 0 -15px;
  @include media('<md') {
    margin: 0;
  }

  &-link {
    padding: 0;
    margin-left: 25px;
    font-size: 12px;
    text-transform: uppercase;
    color: $color--white;
    &:hover {
      color: darken($color--white,9)
    }

    &--green{
      color: $color--green;
      &:hover {
        color: lighten($color--green, 9);
      }
    }
  }
}
</style>
