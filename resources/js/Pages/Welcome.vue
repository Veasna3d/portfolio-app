<script setup>
import { Head, Link } from '@inertiajs/inertia-vue3';
import FrontendLayout from '@/Layouts/Frontend.vue';
import Hero from '@/Components/Frontend/Hero.vue';
import Promote from '@/Components/Frontend/Promote.vue';
import About from '@/Components/Frontend/About.vue';
import Skills from '@/Components/Frontend/Skill.vue';
import Portfolio from '@/Components/Frontend/Portfolio.vue';
import Service from '@/Components/Frontend/Service.vue';
import Contact from '@/Components/Frontend/Contact.vue';

defineProps({
    skills: Object,
    projects: Object,
})
</script>

<template>
    <Head title="Welcome" />
    <FrontendLayout>
    <!--Hero Section-->
    <Hero />
    <!--Promote Section-->
    <Promote />
    <!--About Section-->
    <About />
    <!--Skill Section-->
    <Skills :skills="skills" />
    <!--Portfolio-->
    <Portfolio :skills="skills" :projects="projects" />
    <!--Service Section-->
    <Service /> 
    <!--Contact Section-->
    <Contact /> 
    </FrontendLayout>
</template>
