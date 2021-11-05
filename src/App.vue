<template>
  <div id="app" class="container">
    <div class="row py-4">
      <CvSatu /><br><br>
      <CvDua />
    </div>
  </div>
</template>

<script>
  import CvSatu  from './components/CvSatu.vue'
  import CvDua from './components/CvDua.vue'

  export default {
    name: 'app',
    components: {
      CvSatu,
      CvDua,
    }
  }
</script>
