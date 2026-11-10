<script setup lang="ts">
import { onMounted } from 'vue'
import { storeToRefs } from 'pinia'
import { RouterLink, RouterView } from 'vue-router'
import { useDeliveryStore } from './store'
const store = useDeliveryStore()
const { approvedShare, offers, urgent } = storeToRefs(store)
onMounted(store.load)
</script>

<template><div class="shell"><aside><div class="brand">BuyStrategicEU<span>PROCUREMENT CASES</span></div><nav><RouterLink to="/">Procurement cases</RouterLink><RouterLink to="/insights">Buying guidance</RouterLink></nav><div class="health"><i /> Java procurement service connected</div></aside><main><header><div><span class="eyebrow">Turn public spending into measurable resilience, sustainability and European value</span><h1>Strategic Public Procurement Desk</h1></div><button @click="store.addOffer">Add procurement case</button></header><section class="summary"><article><small>Cases approved</small><strong>{{ approvedShare }}%</strong><div class="bar"><span :style="{ width: `${approvedShare}%` }" /></div></article><article><small>Cases tracked</small><strong>{{ offers.length }}</strong><p>Shared buying view</p></article><article><small>Urgent sourcing gaps</small><strong>{{ urgent }}</strong><p>Needs attention</p></article></section><RouterView /></main></div></template>
