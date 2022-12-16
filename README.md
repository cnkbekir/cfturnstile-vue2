# Cloudflare Turnstile Widget Component for Vue 2

A Vue 2.7 component for showing the Cloudflare Turnstile widget on your project.

## What is Cloudflare Turnstile?
Cloudflare Turnstile is a CAPTCHA alternative from Cloudflare. It uses PAT protocol to verify the user’s devices, preventing bots and malicious users from accessing your site and ensuring your and your visitors’ privacy is protected.

[Introduction for Cloudflare Turnstile](https://blog.cloudflare.com/turnstile-private-captcha-alternative/)

## Installation & Usage

```bash
yarn add cfturnstile-vue2
# or
npm install cfturnstile-vue2
```

```vue
<template>
  <div id="app">
    <cfturnstile
      :sitekey="sitekey"
      @verify="verify"
    />
  </div>
</template>
<script>
import { defineComponent } from 'vue'
import Turnstile from 'cfturnstile-vue2'

export default defineComponent({
  name: 'App',
  components: {
    'cfturnstile': Turnstile
  },
  data() {
    return {
      sitekey: 'YOUR_SITE_KEY'
    }
  },
  methods: {
    verify(token) {
      console.log(token)
    }
  }
})
</script>
```
