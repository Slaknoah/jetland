<template>
  <nav role="navigation">
    <div class="menuToggle">
      <input type="checkbox" />

      <div class="hamburger">
        <span></span>
        <span></span>
        <span></span>
      </div>

      <ul class="menu">
        <li>
          <j-link
            hover-type="underline"
            to="$"
          >
            инвесторам
          </j-link>
        </li>
        <li>
          <j-link
            hover-type="underline"
            to="$"
          >
            предпринимателям
          </j-link>
        </li>
        <li>
          <j-link
            hover-type="underline"
            to="$"
          >
            о платформе
          </j-link>
        </li>
        <li>
          <j-link
            hover-type="underline"
            to="$"
          >
            новости
          </j-link>
        </li>

        <li>
          <JButton class="menu__button" to="/login">
            <div>
              Войти
            </div>
            <login-icon></login-icon>
          </JButton>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import LoginIcon from '../icons/LoginIcon.vue'
export default {
  components: { LoginIcon },

}
</script>

<style lang="scss" src="./menu.scss"></style>