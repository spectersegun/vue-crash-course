<template>
  <button
    @click="$emit('btn-click')"
    :style="{ background: color }"
    class="btn"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: {
      type: String,
    },
    color: {
      type: String,
    },
  },
  methods: {
    onClick() {
      this.$emit('toggle-add-task');
    },
  },
};
</script>
