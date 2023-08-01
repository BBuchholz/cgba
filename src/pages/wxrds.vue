<script setup>
import { ref } from 'vue'

import StepInStone from '~/components/StepInStone.vue'

const testWxrds = ref([
  {
    wxrdvalue: 'SCA',
    wxrdtype: 'CGBuilding',
    content: 'Sylfan Circle Academy',
    related: '',
    uuid: '',
    image: '', // TODO: put logo here
  },
  {
    wxrdvalue: 'SCS',
    wxrdtype: 'CGBuilding',
    content: 'Sonic Circle Syndicated', // TODO: modify all refs to "Sonic Circle Shell"
    related: '',
    uuid: '',
    image: '', // TODO: put logo here
  },
  {
    wxrdvalue: 'STS',
    wxrdtype: 'CGBuilding',
    content: 'Shepton Transmission Services',
    related: '',
    uuid: '',
    image: '', // TODO: put logo here
  },
])
</script>

<template>
  <h1>owAob</h1>

  <p>Our Wxrds Are Our Building</p>

  <StepInStone
    v-for="wxrd in testWxrds"
    :key="wxrd.uuid"
    :uuid="wxrd.uuid"
    :wxrdvalue="wxrd.wxrdvalue"
    :wxrdtype="wxrd.wxrdtype"
    :content="wxrd.content"
    :related="wxrd.related"
    :image="wxrd.image"
  />
</template>
