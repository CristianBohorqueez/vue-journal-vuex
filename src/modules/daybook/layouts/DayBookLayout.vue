<template>
  <div>
    <Navbar />
    <div class="d-flex">
      <div class="col-4">
        <EntryList />
      </div>
      <div class="col">
        <router-view />
      </div>
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue';

export default {
  name: 'DayBookLayout',
  components: {
    Navbar: defineAsyncComponent(() => import('../components/NavBar')),
    EntryList: defineAsyncComponent(() => import('../components/EntryList')),
  },
};
</script>

<style scoped></style>
