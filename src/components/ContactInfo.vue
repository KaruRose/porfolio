<template>
  <div class="contact-info">
    <h5 class="text-h5 text-uppercase text-deep-purple-accent-1">{{ header }}</h5>
    <div class="contact-info__item mt-3" v-for="(item, i) in data" :key="i">
      <div class="contact-info__icon">
        <v-icon size="x-large">{{ item.icon }}</v-icon>
      </div>
      <div class="contact-info__content">
        <span class="text-uppercase text-button">{{ item.title }}</span>
        <a :href="item.href" :target="item.target">{{ item.value }}</a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineComponent, reactive } from 'vue';

defineComponent({
  name: 'ContactInfo',
})

defineProps({
  header: String
})

const data = reactive([
  // {
  //   icon: 'mdi-cellphone-sound',
  //   title: 'Phone',
  //   value: '+ 58 414 3760 987',
  //   href: 'tel:+584143760987',
  //   target: null,
  // },

  {
    icon: 'mdi-gmail',
    title: 'Gmail',
    value: 'rosasdavid60@gmail.com',
    href: 'mailto:rosasdavid60@gmail.com',
    target: null,
  },
  {
    icon: 'mdi-gitlab',
    title: 'GitLab',
    value: '@KaruRose',
    href: 'https://gitlab.com/KaruRose',
    target: '_blank',
  },
  {
    icon: 'mdi-github',
    title: 'Github',
    value: '@KaruRose',
    href: 'https://github.com/KaruRose',
    target: '_blank',
  },
 
])
</script>

<style scoped>
.contact-info__item {
  display: flex;
  align-items: flex-end;
}

.contact-info__content {
  display: flex;
  flex-direction: column;
  margin-left: 10px;
}
</style>