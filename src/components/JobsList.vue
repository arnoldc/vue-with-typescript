<template>
    <div class="job-list">
        <ul>
            <li v-for="job in jobs" :key="job.id">
                <h2>{{ job.title }}</h2>
                <p> {{ job.location }} </p>
            </li>   
        </ul>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import Job from '@/types/Job';

export default defineComponent({
    props: {
        jobs: {
            type: Array as PropType<Job[]>,
            required: true,
        },
    },
})
</script>


<style scoped>

</style>