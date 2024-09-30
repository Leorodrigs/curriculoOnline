<template>
  <div class="accordion">
    <div class="accordion-header" @click="toggleAccordion">
      <span class="accordion-title"> {{ title }}</span>
      <img :src="arrow" :class="isOpen ? 'arrow-rotated' : 'arrow-default'" />
    </div>
    <transition name="fade">
      <div v-if="isOpen" class="accordion-content">
        <slot></slot>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "AppAccordion",
  props: {
    title: String,
    isOpen: Boolean,
  },
  data() {
    return {
      arrow: require("../assets/icons/arrow.svg"),
    };
  },
  methods: {
    toggleAccordion() {
      this.$emit("toggle");
    },
  },
};
</script>

<style scoped>
.accordion {
  border: 1px solid #ccc;
  border-radius: 5px;
  margin: 10px 0;
}

.accordion-header {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px;
  cursor: pointer;
}

.accordion-header span {
  flex-grow: 1;
  text-align: center;
  font-weight: bold;
}

.accordion-content {
  padding: 10px;
}

.arrow-rotated {
  transform: rotate(180deg);
  transition: transform 0.3s ease;
  width: 20px;
  height: 20px;
}

.arrow-default {
  width: 20px;
  height: 20px;
  transition: transform 0.3s ease;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
