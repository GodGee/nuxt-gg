<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        nuxt-basic
      </h1>
      <!-- <img src="~assets/image.png" alt="" srcset="" /> -->
      <img src="~assets/nuxt-views-schema.svg" alt="" srcset="" />
      <!-- <el-button>ElementUI</el-button> -->

      <ul>
        <li v-for="move in moveList" :key="move.id">{{ move.name }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      moveList: []
    };
  },
  asyncData(context, callback) {
    // console.log("context: ", context); //不能使用this，改用context,context包含error,query,params等
    // setTimeout(() => {
    //   callback(null, {
    //     moveList: [
    //       { name: "肖恩克的救赎", id: 1 },
    //       { name: "大圣归来", id: 2 },
    //       { name: "当幸福来敲门", id: 3 }
    //     ]
    //   });
    // }, 1000);
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          moveList: [
            { name: "肖恩克的救赎", id: 1 },
            { name: "大圣归来", id: 2 },
            { name: "当幸福来敲门", id: 3 }
          ]
        });
      }, 1000);
    })
      .then(res =>
        callback(null, {
          moveList: res.moveList
        })
      )
      .catch(err => {
        callback(err);
        context.error(err);
      });
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
