<template>
  <nav>
    <ul>
      <li @click="navigateTo('about')">About Us</li>
      <li @click="navigateTo('services')">Our Services</li>
      <li @click="navigateTo('customers')">Our Customers</li>
    </ul>
  </nav>
</template>

<script>
export default {
  methods: {
    navigateTo(page) {
      // Emit an event to notify the parent component of the selected page
      this.$emit('navigate', page);
    }
  }
};
</script>

<style scoped>
/* Add your custom styles for the navigation bar here */
</style>
