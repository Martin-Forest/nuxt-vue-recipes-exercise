<template>
    <section class="recipes">
        <Recipe
            v-for="recipe in recipes"
            :key="recipe.id"
            :thumbnail="recipe.thumbnail"
            :title="recipe.title"
            :id="recipe.id"
            :previewText="recipe.previewText"/>    
    </section>
</template>

<script>
    import Recipe from '@/components/Recipe'

    export default {
        components: {
            Recipe
        },
        asyncData() {
            return new Promise((resolve,reject) => {
                setTimeout(() => {
                    resolve({
                        recipes: [
                            {
                                id: "1",
                                title: "Delicious chicken",
                                previewText: "Awesome pressure-cooked chicken!!!",
                                thumbnail: "http://www.seriouseats.com/images/2015/09/20150914-pressure-cooker-recipes-roundup-09.jpg"
                            },
                           {
                                id: "2",
                                title: "Awesome beef stew",
                                previewText: "Delicious pressure-cooked beef stew. Yummy!!!",                                
                                thumbnail: "http://worldwidetrophyadventures.com/blog/wp-content/uploads/2016/10/earls-stew.jpg"
                            }                            
                        ]
                    })
                },1500)
            })
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