<template>
  <div>
    
    <button @click="change('ko')">한글</button> &nbsp; <button @click="change('en')">영어</button>
    
    <p>{{ $t('hello') }}</p>
    <p>{{ $t('message') }}</p>
    <p>{{ $t('test') }}</p>
  </div>
</template>

<script>
import i18n from '@/i18n'

export default {
  name: 'HelloI18n',


  methods : {
    change(locale) {
      if(locale === 'ko'){
        i18n.locale = 'ko';
      } else if(locale === 'en'){
        i18n.locale = 'en';
      }
    }
  }
}

</script>

<i18n>
{
  "en": {
    "hello": "Hello i18n in SFC!"
  },

  "ko" : {
    "hello": "안녕하세요"
  }
}
</i18n>
