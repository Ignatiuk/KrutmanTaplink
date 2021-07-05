<template>
  <div class="link-button" @click="onLinkClick">
    <img class="link-button__icon" :src="require(`@/assets/img/icons/${icon}.svg`)" />

    <div class="link-button__body">
      <div class="link-button__title">{{ title }}</div>
      <div class="link-button__description">{{ description }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LinkButton',

  props: {
    title: {
      type: String,
      required: true,
    },

    description: {
      type: String,
      required: true,
    },

    icon: {
      type: String,
      required: true,
    },

    url: {
      type: String,
      required: true,
    },
  },

  methods: {
    onLinkClick() {
      window.open(this.url)
    },
  },
}
</script>

<style lang="scss">
.link-button {
  background-color: #FFC107;
  color: white;
  display: flex;
  cursor: pointer;
  margin: 0 auto;
  padding: 16px;
  border-radius: 16px;

  &__icon {
    height: 42px;
    width: 42px;
    margin-right: 12px;
  }

  &__body {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  &__title {
    font-weight: 600;
  }
}
</style>