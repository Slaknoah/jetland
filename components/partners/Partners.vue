<template>
  <section class="partners">
    <div class="container">
      <h2 class="partners__header">
        <span>СМИ о нас</span>
        <span class="partners__header--highlight"><span class="hide-mobile">Наши</span> партнеры</span>
      </h2>

      <div class="partners__list">
        <a href="#" class="partners__list-item">
          <ForbesLogo />
        </a>

        <a href="#" class="partners__list-item">
          <CommercantLogo />
        </a>

        <a href="#" class="partners__list-item">
          <RBKLogo />
        </a>

        <a href="#" class="partners__list-item">
          <VedomostiLogo />
        </a>

        <a href="#" class="partners__list-item">
          <VCLogo />
        </a>

        <a href="#" class="partners__list-item">
          <RepublicLogo />
        </a>

        <a href="#" class="partners__list-item">
          <BankiLogo />
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import ForbesLogo from '~/components/logos/ForbesLogo';
import CommercantLogo from '~/components/logos/CommercantLogo';
import RBKLogo from '~/components/logos/RBKLogo';
import VedomostiLogo from '~/components/logos/VedomostiLogo';
import VCLogo from '~/components/logos/VCLogo';
import RepublicLogo from '~/components/logos/RepublicLogo';
import BankiLogo from '~/components/logos/BankiLogo';

export default {
  components: {
    ForbesLogo,
    CommercantLogo,
    RBKLogo,
    VedomostiLogo,
    VCLogo,
    RepublicLogo,
    BankiLogo
  }
}
</script>
<style lang="scss" src="./partners.scss"></style>