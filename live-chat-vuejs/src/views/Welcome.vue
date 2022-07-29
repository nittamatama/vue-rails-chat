<template>
  <div>
    <h1>{{ title }}</h1>
    <p v-if="isEnabled">{{ subtitle }}</p>
    <button @click="toggle">トグルする</button>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: '初めてのvue',
      subtitle: 'ようこそ',
      isEnabled: true
    }
  },
  computed: {
    text() {
      if (this.isEnabled) {
        return 'こんにちは'
      } else {
        return 'さようなら'
      }
    }
  },
  methods: {
    toggle() {
      this.isEnabled = !this.isEnabled
    }
  }
}
</script>