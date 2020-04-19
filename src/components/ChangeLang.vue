<template>
    <div class="ab-locale-changer">
        <select v-model="$i18n.locale" @change="getLocale" v-b-tooltip.hover :title="$t('change-lang-title')">
            <option v-for="(lang, i) in langs" :key="i" :value="lang">{{ lang }}</option>
        </select>
    </div>
</template>

<script>
export default {
  name: 'locale-changer',
  data () {
    return { langs: ['ua', 'en'] }
  },
  methods: {
    getLocale (val) {
      localStorage.name = val.target.value
    }
  }
}
</script>
