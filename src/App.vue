<template>
  <div class="app">
   <JobList :jobs="jobs" />
  </div>
  <button @click="changeName('hola')">Change message</button>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref } from 'vue';
import Job from './types/Job';
import JobList from './components/JobsList.vue';

export default defineComponent({
  name: 'App',
  components: { JobList },
  setup() {
    const jobs = ref<Job[]>([
      {
        title: "farm worker",
        location: "ranch",
        salary: 3000,
        id: "1"
      },
      {
        title: "dish worker",
        location: "restaraunt",
        salary: 3000,
        id: "2"
      },
    ]);

    return {
      jobs,
    }


    // const state = reactive({
    //   message: 'Hello Vue!',
    // });


    // return {
    //   ...toRefs(state)
    // }'

    // const name = ref('Vue');
    // const age = ref<string|number>(18);

    // return {
    //   name,
    //   age,
    // } 
  },
});
</script>

<style>

</style>
