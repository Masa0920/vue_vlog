<template>
   <div>
      <b-col>
         <b-card 
         :title="title"
         :img-src="img"
         img-alt="Image"
         img-top
         tag="article"
         style="max-width: 20rem;"
         class="mb-2"
         :footer="footer"
         >
         <b-card-text> {{cardText}} </b-card-text>

         <router-link :to="link">
            <b-button
               v-b-tooltip.hover
               title="Tooltip content"
               v-b-modal="modalId"
               variant="primary"
               >記事を見る</b-button
            >
         </router-link>
         <!-- <b-modal :id="modalId" title="BootstrapVue">
            <p class="my-4">Hello from modal!</p>
         </b-modal> -->
         </b-card>
      </b-col>
   </div>
</template>

<script>
   export default {
      props: ["title", "img", "cardText", "link", "footer"]
   };
</script>

<style scoped></style>
