<template>
  <nuxt-link :to="href" class="flex justify-around flex-no-shrink relative no-underline text-blue-lighter hover:text-blue-lightest hover:bg-blue-light py-3 lg:pl-1">
    <i :class="icon" class="w-1/4 lg:pl-3 fas text-lg"></i>
    <div class="w-3/4 hidden lg:inline-block font-light text-sm"><slot/></div>
    <i class="hidden fas fa-caret-left text-lg absolute pin-r text-white"></i>
  </nuxt-link>
</template>

<script>
export default {
  name: 'NavItem',
  props: {
    href: {
      type: String,
      required: true
    },
    icon: {
      type: String,
      required: false,
      default: 'sun'
    }
  }
}
</script>

<style lang="postcss" scoped>
  .flex {
    cursor: pointer;
  }
  .nuxt-link-active {
    color: config('colors.blue-darker');
  }
  .nuxt-link-active .fa-caret-left {
    display: inline;
  }
</style>
