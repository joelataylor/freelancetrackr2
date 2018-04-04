<template>
  <div class="ft-logo fixed pin-b mb-4 w-16 lg:w-48">
    <div class="block lg:border-t border-blue-light pt-4 mx-4 text-right text-3xl leading-none">
      <p><i class="fab fa-pied-piper"></i></p>
      <p class="font-bold tracking-tight ml-4 hidden lg:inline-block">Freelance <span class="font-bold">Trackr</span></p>
    </div>
  </div>
</template>

<style>
.ft-logo {
  animation: slide 1s ease-in 1s forwards;
  transform: translate(-25%, 0);
}

@keyframes slide {
  100% {
    transform: translate(0, 0);
  }
}
</style>
