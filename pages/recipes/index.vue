<template>
    <section class="recipes">
        <Recipe 
            thumbnail="http://www.seriouseats.com/images/2015/09/20150914-pressure-cooker-recipes-roundup-09.jpg"
            title="Delicious chicken"
            previewText="Awesome pressure-cooked chicken!!!"/>
        <Recipe 
            thumbnail="http://worldwidetrophyadventures.com/blog/wp-content/uploads/2016/10/earls-stew.jpg"
            title="Awesome beef stew"
            previewText="Delicious pressure-cooked beef stew. Yummy!!!"/>       
    </section>
</template>

<script>
    import Recipe from '@/components/Recipe'

    export default {
        components: {
            Recipe
        }
    }
</script>

<style scoped>
.recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
}
</style>