<style>
.liste{
    list-style-type: none;
    padding-inline-start: 0;
    margin: 1rem;
}

.artContainer{
    display: flex;
    flex-wrap:wrap;
    justify-content: center;
}


</style>
<template>
    <ul class="liste">
        <li class="article" v-for="article in articles" :key="article.id">
            <div class="artContainer container-1" >
                <!-- OPTION 1: la Balise Article en parent affiche les propriétés avec leur attribut article en props dans l'enfant Article -->
                 <!-- <Article
                    :id="article.id"
                    :title="article.title"
                    :subtitle="article.subTitle"
                    :content="article.content"
                    :imageSrc="article.imageSrc"
                    :link="article.link"
                 ></Article>  -->
                
                <!-- OPTION 2: la Balise Article reçoit seulement la propriété article -->
                 <Article :article="article"/>


                
            </div>
        </li>
    </ul>
    
</template>

<script>
import Article from './Article.vue'

export default {
    name: 'ArticleList',
    components: {
        Article,
    },
    data(){
        return {
           articles: [
               
                {   id:0,
                    title: "mon super Titre n°1",
                    subTitle: "Sous Titre",
                    imageSrc: "../public/article1.jpeg",
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ullam placeat laboriosam ut voluptatem dolore quisquam corporis quasi, dolores dignissimos incidunt. Perspiciatis et nesciunt quibusdam, cum animi delectus perferendis eveniet.",
                    link: "https://cdn.pixabay.com/photo/2020/07/23/01/09/field-5430070_960_720.jpg"
                },
                {   id:1,
                    title: "mon super Titre n°2",
                    subTitle: "Sous Titre",
                    imageSrc: "../public/article1.jpeg",
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ullam placeat laboriosam ut voluptatem dolore quisquam corporis quasi, dolores dignissimos incidunt. Perspiciatis et nesciunt quibusdam, cum animi delectus perferendis eveniet.",
                    link: "https://cdn.pixabay.com/photo/2020/07/23/01/09/field-5430070_960_720.jpg"
                },
                {   id:2,
                    title: "mon super Titre n°3",
                    subTitle: "Sous Titre",
                    imageSrc: "../public/article1.jpeg",
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ullam placeat laboriosam ut voluptatem dolore quisquam corporis quasi, dolores dignissimos incidunt. Perspiciatis et nesciunt quibusdam, cum animi delectus perferendis eveniet.",
                    link: "https://cdn.pixabay.com/photo/2020/07/23/01/09/field-5430070_960_720.jpg"
                },
                {   id:3,
                    title: "mon super Titre n°4",
                    subTitle: "Sous Titre",
                    imageSrc: "../public/article1.jpeg",
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ullam placeat laboriosam ut voluptatem dolore quisquam corporis quasi, dolores dignissimos incidunt. Perspiciatis et nesciunt quibusdam, cum animi delectus perferendis eveniet.",
                    link: "https://cdn.pixabay.com/photo/2020/07/23/01/09/field-5430070_960_720.jpg"
                },
                {   id:4,
                    title: "mon super Titre n°5",
                    subTitle: "Sous Titre",
                    imageSrc: "../public/article1.jpeg",
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ullam placeat laboriosam ut voluptatem dolore quisquam corporis quasi, dolores dignissimos incidunt. Perspiciatis et nesciunt quibusdam, cum animi delectus perferendis eveniet.",
                    link: "https://cdn.pixabay.com/photo/2020/07/23/01/09/field-5430070_960_720.jpg"
                },
            ],  
        }
    },
     mounted(){
        console.log(this.articles)
        
        
    },
    
}
</script>