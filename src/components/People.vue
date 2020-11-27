<template>
    <div class="container">
        <div class="people">
            <Person v-for="person in people" :key="person.id" :name="person.name" :email="person.email" :id="person.id" />
        </div>
    </div>
</template>

<script>
import Person from './Person.vue'
import axios from "axios"

export default {
    name: 'People',
    data () {
        return {
            people: [],
        }
    },
    mounted (){
        axios({method: "GET", "url": "https://my-user-manager.herokuapp.com/users"})
        .then(result => {
            this.people = result.data;
        }, 
        error => {console.error(error);});
    },
    components: {
        Person
    }
}
</script>

<style scoped>
    @import '../assets/styles/people-styles.css';
</style>