<template>
    <div>
        <article :username="user.name" @click="user_clicked" v-for="user in users" :key="user.id">   
            <h3>{{user.name}}</h3>
            <p>{{user.age}}</p>
            <p>{{user.is_premium}}</p>
        </article>
    </div>
</template>

<script>
    export default {
        props: {
            users: Array,
        },
        methods: {
            user_clicked: function(event) {
                let selected_user = event.currentTarget.getAttribute(`username`);
                this.$emit(`user_clicked`, selected_user);
            }
        }
        }
</script>

<style scoped>

</style>