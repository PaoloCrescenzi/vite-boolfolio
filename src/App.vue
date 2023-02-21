<script>
import TheMain from './components/TheMain.vue';
import axios from 'axios';
	export default {
    components: {TheMain},
    data() {
      return {
        backendurl: 'http://127.0.0.1:8000',
        projects:[],
      };
    },
    methods:{
      fetchProjects(){
        axios.get(this.backendurl + "/api/projects/")
        .then((resp)=>{
          this.projects = resp.data;
        })
      }
    },
    mounted(){
      this.fetchProjects();
    }
	}
</script>

<template>
  <TheMain></TheMain>
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
  @use "styles/main";
  @use "bootstrap/scss/bootstrap";
</style>
