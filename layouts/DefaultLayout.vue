<template>
  <div>
    <TheHeader />
    <nuxt/>
    <div>footer</div>
  </div>
</template>

<script>
import TheHeader from "@/components/TheHeader"
export default {
    name:'DefaultLayout',
    components: {TheHeader }
}
</script>
