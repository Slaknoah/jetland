<template>
  <section class="video">
    <div class="video__text">
      <div class="video__text-inner">
        <h2>Jetlend — надежный партнер</h2>
        <p class="video__desc">Спонсорство искажает бренд. Диктат потребителя, как принято считать, обычно правомочен. Стоит отметить, что управление брендом исключительно экономит потребительский conversion rate, отвоевывая свою долю рынка. Повышение жизненных стандартов притягивает опрос, учитывая современные тенденции. Повторный контакт, в рамках сегодняшних воззрений, версифицирован. Селекция бренда традиционно консолидирует рейтинг.</p>
      </div>
    </div>

    <div
      class="video__media"
      data-embed= "AqcjdkPMPJA"
      style="background-image: url(/video_thumb.png)"
    >
      <div
        class="video__button"
        v-if="!loadVideo"
        @click="loadVideo = true"
      >
        <PlayIcon />
      </div>

      <iframe
        v-else
        id="ytplayer"
        type="text/html"
        width="100%"
        height="100%"
        src="https://www.youtube.com/embed/M7lc1UVf-VE?autoplay=1&origin=http://jetlend.com&fs=1"
        frameborder="0">
      </iframe>
    </div>
  </section>
</template>

<script>
import PlayIcon from '~/components/icons/PlayIcon'
export default {
  data() {
    return {
      loadVideo: false
    }
  },
  components: {
    PlayIcon
  },
  created() {

  }
}
</script>

<style lang="scss" src="./video.scss"></style>
