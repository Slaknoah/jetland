<template>
  <section class="calculator" :style="`padding-top: ${cardHeight}`">
    <div class="container">
      <div class="calculator__card" ref="calculatorCard">
        <h2 class="calculator__header">Калькулятор заемщика</h2>

        <div class="calculator__content">
          <div class="calculator__form">
            <div class="calculator__input">
              <JInputSlider
                label="Желаемая сумма кредита"
                v-model="form.creditSum"
                :is-price="true"
                min="500000"
                max="10000000"
                suffix="₽"
              />

              <div class="calculator__append">
                <p>500 000 руб.</p>
                <p>10 000 000 руб.</p>
              </div>
            </div>

            <div class="calculator__input">
              <JInputSlider
                label="Срок кредита"
                v-model="form.creditDur"
                min="1"
                max="12"
                suffix="мес."
              />
              <div class="calculator__append">
                <p>1 месяц</p>
                <p>12 месяцев</p>
              </div>
            </div>
          </div>
          <div class="calculator__result">
            <div class="calculator__result-label">Ежемесячный платеж</div>
            <div class="calculator__result-value">
              <div>{{ result |formatCurrency }} </div>
              <div class="underline"></div>
            </div>
            <j-button
              to="#"
              class="calculator__button"
            >
              Получить кредит
            </j-button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cardHeight: '0px',
      form: {
        creditSum: 1000000,
        creditDur: 5
      },
      interest: 110/100
    }
  },
  computed: {
    result() {
      return this.interest * ( this.form.creditSum / ( this.form.creditDur ) );
    }
  },
  methods: {
    setCardHeight() {
      if( this.$refs.calculatorCard ) {
        const windowWidth  = window.innerWidth || document.documentElement.clientWidth ||
                        document.body.clientWidth;
        const offSet = ( windowWidth >= 768 ) ? 211 : 59;
        this.cardHeight = this.$refs.calculatorCard.clientHeight - offSet + 'px';
      }
    }
  },
  mounted() {
    this.setCardHeight();
    window.addEventListener("resize", this.setCardHeight);
  }
}
</script>

<style lang="scss" src="./calculator.scss"></style>
