<template>
  <div class="taplink">
    <div class="taplink__avatar-wrapper">
      <img :src="require(`@/assets/img/ava.png`)" alt="Avatar" class="taplink__avatar">
    </div>

    <LinkButton
      v-for="link in links"
      :key="link.title"
      v-bind="link"
      class="taplink__link"
    />
  </div>
</template>

<script>
import LinkButton from '@/components/LinkButton/LinkButton'

export default {
  name: 'App',

  components: { LinkButton },

  data() {
    return {
      links: [
        {
          title: 'Донатик',
          description: 'Буду рад каждому донату 🙋‍♀️',
          url: 'https://www.donationalerts.com/r/krutman',
          icon: 'donation',
        },

        {
          title: 'Telegram 💤',
          description: 'Частые конкурсы 🌈',
          url: 'https://t.me/brawl_stars_world',
          icon: 'telegram',
        },

        {
          title: 'Discord',
          description: 'Общаюсь с подписотой ✊',
          url: 'https://discord.com/invite/ucNAM3FZy9',
          icon: 'discord',
        },

        {
          title: 'Instagram 🎈',
          description: 'За рекламой сюды 🤷‍♀️',
          url: 'https://www.instagram.com/hyqqee/',
          icon: 'instagram',
        },
      ],
    }
  },
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@400;700&display=swap');

body,
html {
  font-family: 'Ubuntu', sans-serif;
  margin: 0;
  padding: 8px;
}

.taplink {
  max-width: 800px;
  margin: 0 auto;

  &__avatar {
    height: 100px;
    margin: 0 auto;

    &-wrapper {
      width: 100%;
      display: flex;
      align-items: center;
      margin-bottom: 12px;
    }
  }

  &__link:not(:last-child) {
    margin-bottom: 16px;
  }
}
</style>
