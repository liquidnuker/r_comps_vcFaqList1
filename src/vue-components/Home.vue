<template>
  <div>
    <!-- vcFaqList1-01 placeholder -->
    <h2 class="item-id">vcFaqList1-01</h2>
    <div class="row">
      <div class="col-sm-3">39</div>
      <div class="col-sm-9">
      <!-- vcFaqlist1-01 mount -->
        <div id="vcFaqList1-01_mount"></div>
      <!-- end vcFaqlist1-01 mount -->
      </div>
    </div>
    <!-- end vcFaqList1-01 placeholder -->
  </div>
</template>
<script>
import {inject} from "../js/componentinjector.js";
  export default {
    data () {
      return {    
      }
    },
    mounted: function () {
      this.mountFaqList1_01();
    },
    methods: {
      mountFaqList1_01: function() {
        const vcFaqlist1_01 = resolve => {
          require.ensure(['./vcFaqlist1_01.vue'], () => {
            resolve(require('./vcFaqlist1_01.vue'))
          })
        };
        inject("#vcFaqList1-01_mount", vcFaqlist1_01);
      }
    }
  }
</script>