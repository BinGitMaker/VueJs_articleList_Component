<style>
/* un cadre d'article' */
.box{
  border: 2px solid #333;
  border-radius: 1px 140px / 150px;
  background-color: rgb(255, 221, 203);
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding-block: 3%;
  padding-inline: 3%;
  margin-block: 2rem;
  margin-inline: 30%;
  min-width: 70%;
}

.topArticle{
  display:flex;
  flex-direction: row-reverse;
  justify-content: space-around;  
}


.titleGroup{
    display:flex;
    flex-direction: column;
}

.lgTxt{
    padding: 2rem;
    text-align: start;
}

.link{
    text-align: end;
}

.imageStyle{
    width : 300px;
    max-height : 200px;
}

@media screen and (min-width: 800px){
    .topArticle{
    display:flex;
    flex-direction: column;
    justify-content: space-around;  
    }
    
}

</style>

<template>

    <div idd="app" class="box box-1 article"> 

        <div class="topArticle">
            <div class="titleGroup article">
                <!-- OPTION 1 : les proprietes sont appellées sans leur attribu article {{ title }}-->
                <!-- OPTION 2 : les proprietes sont appellées avec leur attribu article ex: {{ article.title }}-->
                <h1> {{ article.title }} </h1>
                <h2> {{ article.subTitle }} </h2>
                <div class="lgTxt">
                    <p>{{ article.content }}</p>
                </div>
            </div>
            <div>
                <a :href="article.link">
                    <!-- les src et href doivent etre bindés sans moustache -->
                    <img :src="article.imageSrc" class="imageStyle" alt="image_test"/>
                </a>
            </div>
        </div>   

        <div class="link">
            <a :href="article.link">Article-Link</a>
        </div>

    </div>  

</template>


<script>

export default {
    name: 'Article',
      /* data(){
        return{ // OPTION1 : data pour article
           article: [ 
            this.id, 
            this.title, 
            this.subTitle, 
            this.imageSrc,
            this.content, 
            this.link
            ], 
        }
    },   */
    
     props: { 
        // OPTION 1 : propriétés bindés dans la baslise Article du parent ArticleList
        /* id: Number,
        title: String,     
        subTitle: String,
        imageSrc: String,          
        content: String,
        link: String,  */


        // OPTION2 : on passe seulement article dans la baslise Article du parent ArticleList
        article:Object,
        },
}

</script>