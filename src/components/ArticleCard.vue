<template>
   <div>
      <b-col>
         <div class="card">
            <img class="card-img cover" src="https://picsum.photos/seed/picsum/200/300" alt="">
            <div class="padding-10">
               <p class="font-size-20"> {{title}} </p>
               <p class=""> {{category}} </p>
               <p class=""> {{date}} </p>
               <router-link :to="link">
                  <b-button
                     v-b-tooltip.hover
                     title="Tooltip content"
                     v-b-modal="modalId"
                     variant="primary"
                     >記事を見る</b-button>
               </router-link>
            </div>
         </div>

      </b-col>
   </div>
</template>

<script>
   export default {
      props: ["title", "category", "date", "link"]
   };
</script>

<style scoped>
.card {
   width: 320px;
   margin: 10px;
}
.card-img {
   width: 318px;
   height: 180px;
}
/* width */
.w50 {
  display: inline-block;
  width: 50px;
  margin: 0 auto;
}
.w100 {
display: inline-block;
width: 100px;
margin: 0 auto;
}
.w150 {
display: inline-block;
width: 150px;
margin: 0 auto;
}
.w100p {
width: 100%;
}
.w200 {
display: inline-block;
width: 200px;
margin: 0 auto;
}
.w250 {
display: inline-block;
width: 250px;
margin: 0 auto;
}
.w300 {
display: inline-block;
width: 300px;
margin: 0 auto;
}
.w400 {
display: inline-block;
width: 400px;
margin: 0 auto;
}
.w450 {
display: inline-block;
width: 450px;
margin: 0 auto;
}
.w500 {
display: inline-block;
width: 500px;
margin: 0 auto;
}
.w90vw {
  width: 90vw;
  border-radius: 5px;
  margin: 0 auto;
}
.w70vw {
  width: 70vw;
  border-radius: 5px;
  margin: 0 auto;
}

.w600 {
  width: 600px;
  margin: 0 auto;
}
.w700 {
  max-width: 700px;
  width: 70vw;
  margin: 0 auto;
}

/* padding */
.padding-5 {padding: 5px;}
.padding-10 {padding: 10px;}
.padding-20 {padding: 20px;}
.padding-10-20 {padding: 10px 20px;}

/* margin */
.margin-auto {margin: 0 auto;}
.margin-10-auto {margin: 10px auto;}
.margin-5 {margin: 5px;}
.margin-0-5 {margin: 0 5px;}
.margin-10 {margin: 10px;}
.margin-20 {margin: 20px;}

/* 背景設定用 */
.back-grey {background-color: rgb(240, 240, 240);}
.back-grey2 {background-color: rgb(220, 220, 220);}
.back-silver {background-color: silver;}
.back-white {background-color: white;}
.back-skyblue {background-color: skyblue;}
/* .back- {background-color: ;} */

/* border */
.border {
border-radius: 5px;
}
.border-grey {
border: solid 2px rgb(240, 240, 240);
border-radius: 5px;
}
.border-grey2 {
border: solid 2px rgb(220, 220, 220);
border-radius: 5px;
}
/* color */
.white {color: white;}
.skyblue {color: skyblue;}
.blue {color: #007bff;}
.green{color: #28a745;}
.red{color: #dc3545;}
.pink{color: rgb(255, 0, 255);}
/* . {color: ;} */

/* fontsize */
.font-size-small {font-size: 14px;}
.font-size-20 {font-size: 20px;}
.font-size-100 {font-size: 100px;}
.font-size-h2 {font-size: 24px;}
.font-size-h1 {font-size: 32px;}
/* .font-size- {font-size: px;} */

/* fontweight */
.font-weight-600 {font-weight: 600;}

/* textAlign */
.right {text-align: right;}
.left {text-align: left;}
.center {text-align: center;}

.blank {height: 50px;}
.blank-small  {height: 30px;}

/* img */
.img-contain {object-fit: contain;}
.img-cover {object-fit: cover;}
</style>
