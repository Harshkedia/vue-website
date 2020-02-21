<template>
    <div>
        <b>With</b>: <a v-for="col in collaborators" :key="col.name" :href="col.link" class='col'>{{col.name}}</a>
    </div>
</template>


<script>
export default {
    name: "Collaborators",
    props: {
        collaborators: Array
    }
}
</script>

<style scoped>
    .col{
        text-decoration: none;
        color: red;
    }
    .col:hover{
        color: black;
    }
</style>

