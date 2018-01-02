<template lang="html">
          <div class="offer">
            <header class="offer__header">
              <img class="offer__image" src="../assets/img/img-person.jpg" alt="">
              <div class="offer__content">
                <h3>Profil zweryfikowany przez : <span class="text--green">Lorem ipsum</span></h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer tincidunt iaculis turpis, sed fringilla justo semper sed. Morbi non ultrices magna, vel euismod libero. Pellentesque blandit ornare </p>
                <div class="offer__ratings">
                  <span class="offer__star offer__star--active"></span>
                  <span class="offer__star offer__star--active"></span>
                  <span class="offer__star offer__star--active"></span>
                  <span class="offer__star offer__star--active"></span>
                  <span class="offer__star"></span>
                </div>
                <span class="offer__average">Średnia ocena: 4</span>
              </div>
            </header>
            <h2 class="offer__profession">Programista</h2>
            <ul class="offer__list">
              <li class="offer__info">
                <h4>Branża:</h4>
                <p>IT- Rozwój oprogramowania</p>
              </li>
              <li class="offer__info">
                <h4>Destynacja:</h4>
                <p>Zdalnie</p>
              </li>
              <li class="offer__info">
                <h4>Wynagrodzenie: </h4>
                <p>12000</p>
              </li>
              <li class="offer__info">
                <h4>Dostępność:</h4>
                <p>za miesiąc</p>
              </li>
              <li class="offer__info">
                <h4>Języki: </h4>
                <p>Angielski, Polski </p>
              </li>
              <li class="offer__info">
                <h4>Cena za zweryfikowany&nbsp;profil:</h4>
                <p>500zl</p>
              </li>
            </ul>
            <div class="offer__buttons">
              <button class="btn btn-primary btn-block" type="button" >Zobacz pełny opis</button>
              <button class="btn btn-secondary btn-small" type="button" >Dodaj do katalogu</button>
              <button class="btn btn-secondary btn-small" type="button" >Dodaj do kosza</button>
            </div>
          </div>
</template>

<style lang="scss" scoped>
@import '../styles/helpers/colors.scss';
@import '../styles/helpers/include-media.scss';

.offer {
  background-color: $color--white;
  width: 532px;
  margin: 20px auto 50px;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 2px 30px 0 rgba(0,0,0,0.22);
  padding-bottom: 20px;
  @include media('<lg') {
    box-shadow: 0 2px 2px 2px rgba(0, 0, 0, 0.22);
  }
  @include media('<md') {
    width: 100%;
  }

  &__header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding-bottom: 16px;
    @include media('<sm') {
      flex-direction: column;
      text-align: center;
    }
  }
  &__image {
    max-width: 150px;
    @include media('<sm') {
      margin: 0 auto;
      border-radius: 10px;
      padding-top: 5px;
    }
  }
  &__content {
    padding: 2px 25px 0 24px;
    @include media('<md') {
      padding: 0 10px 0 10px;
    }
  }

  &__ratings {
    padding-top: 6px;
  }
  &__star {
    content: url(../assets/svg/ico-star.svg);
    width: 25px;
    height: 25px;
    margin-right: 12px;
    @include media('<md') {
      width: 20px;
      height: 20px;
    }
    &--active {
      content: url(../assets/svg/ico-star-active.svg);
    }
  }
  &__average {
    font-size: 12px;
  }
  &__profession {
    background-color: $color--green;
    padding: 13px 0;
    text-align: center;
  }
  &__list {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    text-align: center;
    padding: 17px 10px 3px;
  }
  &__info {
    width: 33%;
    padding-top: 15px;
    @include media('<sm') {
      width: 50%;
      padding-top: 5px;
    }
  }
  &__buttons {
    padding: 0 60px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    @include media('<sm') {
      padding: 0 30px;
    }
  }
}
</style>
