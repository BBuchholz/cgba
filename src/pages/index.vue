<script setup lang="ts">
defineOptions({
  name: 'IndexPage',
})
const user = useUserStore()
const anyMyrKi = $ref(user.savedMyrKi)

const router = useRouter()
function go() {
  if (anyMyrKi)
    router.push(`/myrKiSs/${encodeURIComponent(anyMyrKi)}`)
}

const { t } = useI18n()
</script>

<template>
  <div>
    <div py-4 />

    <TheInput
      v-model="anyMyrKi"
      placeholder="enter myrKi..."
      autocomplete="false"
      @keydown.enter="go"
    />
    <label class="hidden" for="input">We require more than a mere key for entry...</label>

    <div>
      <button
        m-3 text-sm btn
        :disabled="!anyMyrKi"
        @click="go"
      >
        {{ t('button.go') }}
      </button>
    </div>
    <img alt="CGBA logo" :src="isDark ? '/CGBA_LOGO-DARK.png' : '/CGBA_LOGO-LIGHT.png'">

    <p>
      <em text-sm opacity-75>Home Base for all Coventry Grove Building Projeckts</em>
    </p>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>

<style>
img {
  max-width: 100%;
  height: auto;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;
  margin-bottom: 20px;
}
</style>
