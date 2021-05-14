<template>
  <section class="main-banner">
    <div class="container">
      <div class="main-banner__content">
        <div class="main-banner__brands">
          <a class="main-banner__brands-item main-banner__brands-item--bank" href="#">
            <BankRussiaLogo />
          </a>

          <a class="main-banner__brands-item main-banner__brands-item--sk" href="#">
            <SKLogo />
          </a>
        </div>

        <div class="main-banner__links">
          <j-link
            hover-type="underline"
            to="#"
            class="main-banner__links-item"
          >
            Обзор
          </j-link>
          <span class="divider"></span>
          <j-link
            hover-type="underline"
            to="#"
            class="main-banner__links-item"
          >
            Условия
          </j-link>
          <span class="divider"></span>
          <j-link
            hover-type="underline"
            to="#"
            class="main-banner__links-item"
          >
            Вопросы
          </j-link>
        </div>

        <div class="main-banner__header">
          <h1>Кредит на пополнение оборотных средств</h1>
        </div>

        <ul class="main-banner__points">
          <li class="main-banner__points-item">
            Сумма до 5 000 000 ₽
          </li>
          <li class="main-banner__points-item">
            Ставка от 11% годовых
          </li>
          <li class="main-banner__points-item">
            Срок до 12 месяцев
          </li>
        </ul>

        <j-button class="main-banner__button">
          Получить кредит
        </j-button>
      </div>
    </div>
  </section>
</template>

<script>
import BankRussiaLogo from '~/components/logos/BankRussiaLogo';
import SKLogo from '~/components/logos/SKLogo';
export default {
  components: {
    BankRussiaLogo,
    SKLogo
  }
}
</script>

<style lang="scss" src="./main-banner.scss"></style>
