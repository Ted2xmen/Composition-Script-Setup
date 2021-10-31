<template>
  <h3>{{title}}</h3>
  <input type="text" v-model="title">
  <button @click="inc">{{counter}} arttır</button>
  <hr>
  <OddOrEven :counter="counter" @odd-event="alertMe" />
</template>



<script setup> // beforeCreate created ve data yerine geçiyor setup
import {ref} from "vue"
import OddOrEven from "./components/OddOrEven.vue"
import Utils from "./composables/Utils"


// composables'A taşındı
  // const title = ref("Başlık")
  // const counter = ref(0)
  // const inc = () => {
  //   counter.value++
  // }
  // const alertMe = (info) => {
  //   console.log(info);
  // }

  const {title, counter, inc, alertMe} = Utils();

</script>
