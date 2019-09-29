<template>
  <div>
    {{ type }}<br />
    <button
      type="button"
      v-on:click.meta="handleClick('cmdCtrl')"
      v-on:click.ctrl="handleClick('cmdCtrl')"
      v-on:click.shift="handleClick('shift')"
      v-on:click.alt="handleClick('alt')"
      v-on:click.exact="handleClick('click')"
    >
      Click with modifier keys (inline)
    </button>
    
    <ModifierClick
      @cmdCtrl="handleClick('cmdCtrl')"
      @click="handleClick('none')"
      @shift="handleClick('shift')"
      @alt="handleClick('alt')"
    />
  </div>
</template>

<script>
import Vue from 'vue';
import ModifierClick from './ModifierClick';

export default {
  components: {
    ModifierClick,
  },
  data() {
    return {
      type: 'none'
    };
  },
  methods: {
    handleClick(type) {
      this.type = type;
    }
  }
};
</script>

<style></style>
