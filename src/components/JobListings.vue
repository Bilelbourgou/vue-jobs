<script setup>
import JobsData from '@/jobs.json';
import JobListing from '@/components/JobListing.vue';
import { ref } from 'vue';

const jobs = ref(JobsData);


</script>
<template>
    <section class="bg-green-50 px-4 py-10">
        <div class="container-xl lg:container m-auto">
            <h2 class="text-3xl font-bold text-green-500 mb-6 text-center">
                Browse Jobs
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <JobListing v-for="job in jobs" :key="job.id" />
            </div>
        </div>
    </section>
</template>