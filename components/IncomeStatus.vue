<template>
  <p class="flex-1 text-blue py-4 border-t-4 border-transparent hover:border-t-4 hover:border-blue-light text-2xl md:text-3xl lg:text-5xl xl:text-6xl">
    <span class="tracking-tight md:tracking-normal block">{{ amount | currency( '$', 0 ) }}</span>
    <span class="text-sm text-grey-dark block">{{ type }}</span>
  </p>
</template>

<script>
export default {
  data() {
    return {
      amount: Math.floor(Math.random() * Math.floor(9999))
    }
  },
  props: {
    type: {
      type: String,
      required: true
    }
  }
}
</script>
