<template>
  <div class="container">
    <h1 class="title">Список курсов</h1>
    <div class="wrapper">
      <div class="card" v-for="item in cards" :key="item.id">
        <div class="card-is-active" v-if="item.isActive">
          <div class="card__title">{{ item.title }}</div>
          <div class="card__description">{{ item.description }}</div>
          <div class="card__duration-course">
            <span>{{ item.duration }}</span> месяцев
          </div>
        </div>
        <div class="card-is-not-active" v-else>
          <div class="card__empty">Кажется, курс уже не существует...</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const cards = ref([
  {
    id: 1,
    title: 'Python-Разработчик',
    description: `
        Описание: На Python пишут сайты, приложения, игры и чат-боты.
        Netflix, Spotify, Google, Dropbox и YouTube написаны на python
        `,
    duration: 10,
    isActive: true,
  },
  {
    id: 2,
    title: 'Графический дизайнер',
    description: `
        Описание: Научим делать бренды узнаваемыми через создание логотипов,
        графики для рекламы, упаковки и не только.
        `,
    duration: 10,
    isActive: true,
  },
  {
    id: 3,
    title: 'Веб-разработчик',
    description: `
        Описание: Веб-разработчик создаёт сайты, сервисы и приложения, которыми
        мы ежедневно пользуемся.
        `,
    duration: 10,
    isActive: true,
  },
  {
    id: 4,
    title: 'Инженер по тестированию',
    description: `
        Описание: Вы научитесь находить ошибки в работе сайтов и приложений
        с помощью Java, JavaScript или Python.
        `,
    duration: 7,
    isActive: true,
  },
  {
    id: 5,
    title: 'Python-Разработчик',
    description: `
        Описание: Кажется, курс уже не существует...
        `,
    duration: 10,
    isActive: false,
  },
  {
    id: 6,
    title: 'Python-Разработчик',
    description: `
        Описание: Кажется, курс уже не существует...
        `,
    duration: 10,
    isActive: false,
  },
  {
    id: 7,
    title: 'Python-Разработчик',
    description: `
        Описание: Кажется, курс уже не существует
        `,
    duration: 10,
    isActive: false,
  },
])
</script>

<style scoped></style>
>
