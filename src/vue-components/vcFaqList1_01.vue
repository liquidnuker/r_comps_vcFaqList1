<template>
  <div>
    <article class="vcFaqList1-01">
      <ul v-for="(i, index) in faqList">
        <li>
          <h2 class="vcFaqList1-01_title"
          v-on:click="toggleContent(index)">
            {{ i.title }}
            <span v-if="!i.toggled">+</span>
            <span v-else>-</span>
          </h2>          
          <section>
            <p v-if="i.toggled">
              {{ i.content }}
            </p>
          </section>
        </li>
      </ul>
    </article>
  </div>
</template>
<script>
export default {
  data () {
    return {
      faqList: [
        {
          title: "vcFaqList1-01_title1",
          content: "Lorem ipsum dolor sit amet1,...",
          toggled: false
        },
        {
          title: "vcFaqList1-01_title2",
          content: "Lorem ipsum dolor sit amet2,...",
          toggled: false
        }
      ]
    }
  },
  mounted: function() {
    this.toggleAllContent(false);
  },
  methods: {
      toggleContent: function(index) {
        let faqList = this.faqList;
        faqList[index].toggled = !faqList[index].toggled;
      },
      toggleAllContent: function(visible) {
        let faqList = this.faqList;
        for (let i in faqList) {
          faqList[i].toggled = visible;
        }
      }
    }
}
</script>