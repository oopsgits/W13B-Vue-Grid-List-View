<template>
    <div>
        <div id="button" @click="toggleView, toggleButton"  :class="{ 'button' : button }">toggle View</div>
        <div id="tweets" :class="{ 'list-view':listView }">
            <article class="tweet" v-for="(tweet, index) in tweets" :key="index">
               <h4>{{tweet.author}}</h4>
               <h6>{{tweet.date}}</h6>
                <p>{{tweet.text}}</p>
            </article>
        </div>
    </div>
</template>

<script>

export default {
    name: 'vue-tweets',
    data() { 
        return {
            listView: false,
            tweets: [
                {
                author: 'james',
                date: 'december 22 , 2020',
                text: 'Hello World I am a tweet!!'
                },
                {
                 
                author: 'james',
                date: 'december 14 , 2020',
                text: 'Hello World I am a tweet!!'
                },
                { 
                author: 'james',
                date: 'december 32 , 2020',
                text: 'Hello World I am a tweet!!'
                },
                
                
                
            ]
        }
    },
    methods: {
        toggleView(){
           this.listView = !this.listView;
           
        }
    }


}




</script>





<style>

 #tweets{
    display: grid;
    grid-template-columns:repeat(3, 1fr);
    grid-gap: 1rem;
    padding: 1rem;
 }
 #tweets.list-view {
   
    grid-template-columns: 1fr;
 }

 #button { background-color: #4CAF50;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}

#button.listview {
    background-color: #0d6deb;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
    

}

 





 @media only screen and (min-width: 568px){
     #teweets.list-view {
         display: grid;
    grid-template-columns:repeat(3, 1fr);

     }

 }




 .article {
    margin: 0%;
    padding: 0%;
 }
 





</style>

