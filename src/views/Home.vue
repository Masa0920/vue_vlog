<template>
  <b-container>
    <h3>大学の勉強のこと、プログラミングのことなどについて学んだことを記録していく</h3>
    <div class="blank"></div>
    <b-row align-v="center">
        <article-card
          v-for="job in jobs"
          :key="job.id"
          :title="job.title"
          :category="job.category"
          :date="job.date"
          :link="job.link"
        ></article-card>
      </b-row>
  </b-container>
</template>

<script>
// @ is an alias to /src
import ArticleCard from "@/components/ArticleCard.vue";

export default {
  name: 'home',
  components: { 
    "article-card": ArticleCard
  },
  mounted() {
    this.fetchData();  
  },
  data() {
    return {
      jobs: []
    };
  },
  methods: {
    async fetchData() {
      const res = await fetch("jobs.json");
      const val = await res.json();
      this.jobs = val;
    }
  }
}
</script>
<style scoped>
.left {text-align: left;}
/* fontsize */
.font-size-all {font-size: 14px;}
.font-size-20 {font-size: 20px;}
.font-size-100 {font-size: 100px;}
.font-size-h2 {font-size: 24px;}
.font-size-h1 {font-size: 32px;}
/* fontweight */
.font-weight-600 {font-weight: 600;}
.blank {height: 50px;}
.blank-all  {height: 30px;}
.w300 {
display: inline-block;
width: 300px;
margin: 0 auto;
}
</style>