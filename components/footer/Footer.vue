<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__row">
        <div class="footer__col">
          <a class="footer__logo" href="">
            <Logo color="white" />
          </a>

          <div @click.stop="scrollToTop">
            <j-link
              class="footer__arrow"
              hover-type="color"
            >
              <ArrowUpIcon />
            </j-link>
          </div>

          <div class="footer__socials footer__socials--desktop">
            <a href="#">
              <facebook-icon></facebook-icon>
            </a>
            <a href="#">
              <instagram-icon></instagram-icon>
            </a>
            <a href="#">
              <youtube-icon></youtube-icon>
            </a>
            <a href="#">
              <telegram-icon></telegram-icon>
            </a>
          </div>
        </div>

        <div class="footer__col footer__col--desktop">
          <ul class="footer__menu">
            <div class="footer__menu-col">
              <li>
                <j-link to="#" hover-type="underline">инвесторам</j-link>
              </li>
              <li>
                <j-link to="#" hover-type="underline">предпринимателям</j-link>
              </li>
              <li>
                <j-link to="#" hover-type="underline">партнерам</j-link>
              </li>
            </div>

            <div class="footer__menu-col">
              <li>
                <j-link to="#" hover-type="underline">документы</j-link>
              </li>
              <li>
                <j-link to="#" hover-type="underline">о платформе</j-link>
              </li>
              <li>
                <j-link to="#" hover-type="underline">новости</j-link>
              </li>
            </div>
          </ul>
        </div>


        <div class="footer__col">
          <p class="footer__text">
            Москва, территория инновационного центра «Сколково», ул. Нобеля, д. 5, эт/пом/раб 2/8/2
          </p>
        </div>

        <div class="footer__col footer__col--desktop">
          <j-button class="footer__button">
            <div>Войти</div>
            <login-icon></login-icon>
          </j-button>
        </div>

        <div class="footer__col">
          <p class="footer__text">
            © 2018 —2021 Все права защищены <br> ООО «ДжетЛэнд», официальный сайт <br> Лицензия ЦБ РФ №18
          </p>
          <div class="footer__brands">
            <a class="footer__brands-item" href="#">
              <BankRussiaLogo />
            </a>

            <a class="footer__brands-item" href="#">
              <SKLogo />
            </a>
          </div>
        </div>

        <div class="footer__col">
          <div class="footer__socials">
            <a href="#">
              <facebook-icon></facebook-icon>
            </a>
            <a href="#">
              <instagram-icon></instagram-icon>
            </a>
            <a href="#">
              <youtube-icon></youtube-icon>
            </a>
            <a href="#">
              <telegram-icon></telegram-icon>
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import ArrowUpIcon from '../icons/ArrowUpIcon.vue'
import FacebookIcon from '../icons/FacebookIcon.vue'
import InstagramIcon from '../icons/InstagramIcon.vue'
import TelegramIcon from '../icons/TelegramIcon.vue'
import YoutubeIcon from '../icons/YoutubeIcon.vue'
import LoginIcon from '../icons/LoginIcon.vue'

import Logo from '~/components/logos/Logo';
import BankRussiaLogo from '~/components/logos/BankRussiaLogo';
import SKLogo from '~/components/logos/SKLogo';

export default {
  components: {
    Logo,
    SKLogo,
    BankRussiaLogo,

    LoginIcon,
    ArrowUpIcon,
    FacebookIcon,
    YoutubeIcon,
    TelegramIcon,
    InstagramIcon
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: 'smooth'
      });
    }
  }
}
</script>

<style lang="scss" src="./footer.scss"></style>