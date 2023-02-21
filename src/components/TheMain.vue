<script>
import TheHeader from './TheHeader.vue';
import { store } from '../store';

export default {
    components: { TheHeader },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <TheHeader></TheHeader>
    <div class="container">
        <table class=" table">
            <thead>
                <tr>
                    <th>Cover</th>
                    <th>Title</th>
                    <th>Type</th>
                    <th>Technolgy</th>
                    
                </tr>
            </thead>
            <tbody>
                <tr v-for="project in projects" :key="project.id">
                    <div v-if="project.cover_img">
                        <img :src="backendUrl + 'storage/' + project.cover_img" alt="" style="width: 60px;">
                    </div>
                    <td><a :href="'project/' + project.id">{{ project.name }}</a></td>
                    <td>{{ project.description }}</td>
                    <td>{{ project.type }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<style lang="scss">
</style>