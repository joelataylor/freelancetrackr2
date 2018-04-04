<template>
  <div class="client-card">
    <div class="flex flex-col">
      <a href="#" :class="colorClasses" class="no-underline border-t-8 shadow-md hover:border-grey-light">
        <div class="border-b border-l border-r border-grey p-4">
          <div class="flex">
            <div :class="colorClasses" class="flex justify-center items-center text-lg border-2 rounded-full w-12 h-12 font-medium">BA</div>
            <div class="flex flex-col ml-4 mt-1">
              <div class="flex-1 text-black">Bud Abbott</div>
              <div class="flex-1 text-xs text-grey-dark mt-2">Old School Comedy</div>
              <div class="flex-1 text-xs text-grey-dark mt-4">
                <i class="far fa-envelope mr-2"></i>
                <span>bud@abbott.com</span>
              </div>
              <div class="flex-1 text-xs text-grey-dark mt-2">
                <i class="fas fa-phone mr-2"></i>
                <span>111-222-3333</span>
              </div>
            </div>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  computed: {
    colorClasses: function() {
      const colors = ['pink-light', 'purple', 'blue'];
      const rand = Math.floor(Math.random() * colors.length);
      return 'border-' + colors[rand] + ' text-' + colors[rand];
    }
  },
  props: {
    id: {
      type: Number,
      required: true
    }
  }
}
</script>

<style lang="postcss">
  .shadow-md:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.24), 0 4px 4px 0 rgba(0, 0, 0, 0.16);
  }
</style>


