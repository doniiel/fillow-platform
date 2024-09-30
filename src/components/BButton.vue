<template>
  <div class="container">
    <button :style="buttonStyles" @click="handleClick">
      <slot>Click ME!</slot>
    </button>
  </div>
</template>

<script>
export default {
  props: {
    value: String,
    color: {
      type: String,
      default: '#000',
    },
    backgroundColor: {
      type: String,
      default: '#ffffff',
    },
    borderRadius: {
      type: String,
      default: '10px',
    },
    borderSize: {
      type: String,
      default: '1px',
    },
    borderColor: {
      type: String,
      default: '#fff',
    },
    padding: {
      type: String,
      default: '10px 10px',
    },
    gap: {
      type: String,
      default: '10px', 
    },
  },
  computed: {
    buttonStyles() {
      return {
        backgroundColor: this.backgroundColor,
        border: `${this.borderSize} solid ${this.borderColor}`,
        borderRadius: this.borderRadius,
        color: this.color,
        padding: this.padding,
        gap: this.gap, 
      };
    },
  },
  methods: {
    handleClick() {
      this.$emit('buttonClick', this.value); 
    },
  },
};
</script>

<style scoped>
.container {
  margin: 10px;
}

button {
  width: 100%;
  display: flex;
  gap: 10px; 
  outline: none;
  font-size: 18px;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
}

button:hover {
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
}
</style>