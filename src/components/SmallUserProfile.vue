<template>
    <div>
        <article v-for="user in users" :key="user.id">   
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
            }
        }
</script>

<style scoped>

</style>