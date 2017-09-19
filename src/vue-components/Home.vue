<template>
<div>
  <!-- vcFaqList1-01 placeholder -->
  <h2 class="item-id">vcFaqList1-01</h2>
  <div class="row">
    <div class="col-sm-3">39</div>
    <div class="col-sm-9">
      <!-- vcFaqlist1-01 -->
      <vcFaqList101 />
      <!-- end vcFaqlist1-01 -->
    </div>
  </div>
  <!-- end vcFaqList1-01 placeholder -->
</div>
</template>
<script>
const vcFaqList101 = () => import ('./vcFaqList1_01.vue');

  export default {
    data () {
      return {    
      }
    },
    components: {
      vcFaqList101: vcFaqList101
    },
    mounted: function () {
    },
    methods: {
    }
  }
</script>