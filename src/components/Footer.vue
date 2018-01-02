<template lang="html">
  <footer class="footer">
    <div class="container">
      <div class="row justify-content-between footer__row">
        <div class="col-12 col-sm-4">
          <span>Copyright Harex 2017</span>
        </div>
        <div class="col-12 col-sm-8">
          <nav class="footer__nav">
            <ul class="footer__list">
              <li>
                <a href="#" class="footer__link">Regulamin</a>
              </li>
              <li>
                <a href="#" class="footer__link">Polityka prywatności</a>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@import '../styles/helpers/colors.scss';
@import '../styles/helpers/include-media.scss';

.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  font-size: 12px;
  color: $color--white;
  letter-spacing: -0.5px;
  @include media('<md') {
    position: relative;
    text-align: center;
    margin-bottom: 10px;
  }
  &__row {
    margin: 0 -30px;
    align-items: center;
    @include media('<md') {
      margin: 0 0;
    }
    @include media('<sm') {
      flex-direction: column-reverse;
    }
  }

  &__list {
    display: flex;
    justify-content: flex-end;
    @include media('<sm') {
      justify-content: center;
      margin: 15px 0;
    }
  }
  &__link {
    margin-left: 22px;
    font-size: 14px;
    letter-spacing: 0;
    @include media('<sm') {
      margin: 0 10px;
    }
    &:hover {
      color: $color--gray;
      text-decoration: none;
    }
  }
}
</style>
