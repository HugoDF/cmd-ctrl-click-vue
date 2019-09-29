<template>
  <button
    type="button"
    @click.meta="$emit('cmdCtrl')"
    @click.ctrl="$emit('cmdCtrl')"
    @click.shift="$emit('shift')"
    @click.alt="$emit('alt')"
    @click.exact="$emit('click')"
  >
    Click with modifier keys
  </button>
</template>
