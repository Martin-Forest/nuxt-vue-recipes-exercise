<template>
    <section class="single-recipe">
        <h1>{{recipe.title}}</h1>
        <div>
            <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
        </div>
        <p>{{recipe.descriptionText}}</p>
    </section>
</template>

<script>
    export default {
       asyncData(context) {
            return new Promise((resolve,reject) => {
                setTimeout(() => {
                    resolve({
                        recipe: [
                            {
                                id: "1",
                                title: "Delicious chicken",
                                previewtext: "Awesome pressure-cooked chicken!!!",
                                descriptionText: "These are the steps for the detailed recipe.",
                                thumbnail: "http://www.seriouseats.com/images/2015/09/20150914-pressure-cooker-recipes-roundup-09.jpg"
                            },
                           {
                                id: "2",
                                title: "Awesome beef stew",
                                previewtext: "Delicious pressure-cooked beef stew. Yummy!!!",
                                descriptionText: "These are the instructions for the yummy recipe to warm your heart.",                                
                                thumbnail: "http://worldwidetrophyadventures.com/blog/wp-content/uploads/2016/10/earls-stew.jpg"
                            }                            
                        ].find(el => el.id === context.params.id)
                    })
                },1500)
            })
        }       
    }
</script>

<style scoped>
.single-recipe {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
}

.recipe-image {
    width: 100%;
}
</style>