<template>
  
  <section class="container vh-100">
        <div class="bg"></div>
        <div class="bg bg2"></div>
        <div class="bg bg3"></div>
        <div class="d-flex justify-content-around mt-5" data-aos="fade-up">
            <div>
                <h1 class="text-center ms_text_project">PROGETTI</h1>
            </div>
            <div class="d-flex align-items-center">
                <a href="https://github.com/Matteo9099" class="btn btn-warning ms_button_relative">GITHUB</a>
            </div>
        </div>

        <div class="d-flex mt-5 justify-content-center flex-wrap ms_overflow scroller" data-aos="fade-up">
            <!-- inizio -->
            <div v-for="(slide, index) in slides" :key="index" class="m-4 position-relative">
            
                <CardComponent
                    :image="slide.image"
                    :title="slide.title"
                    :content="slide.content"    
                />
                <div class="ms_position_badge">
                    <span v-for="(badge, index) in slide.badges" :key="index" class="badge bg-success me-2">{{ badge }}</span>
                </div>
            </div>
        </div>
        <div class="text-center text-white pt-4 scroll-text"><p>Scroll for more project</p></div>
        
   

  </section>

</template>

<script>
import CardComponent from "../components/CardComponent.vue";

export default {
    name: "ProjectView",
    data() {
        return {
            slides: [
                {
                    image: "bdoctors.png",
                    title: "BDoctors",
                    content: "BDoctors è una web app che permette di cercare un medico specialista e chiedere un appuntamento.",
                    badges: ['Vue', 'Laravel', 'Axios', 'Database'] 
                },
                {
                    image: "boolflix.png",
                    title: "Boolflix",
                    content: "Replica della famosa piattaforma streaming, permette di cercare film e serie tv. La web app richiama tramite API un sito esterno che fornisce i titoli ricercati dall'utente.",
                    badges: ['Vue', 'Axios'] 
                },
                {
                    image: "boolpress.png",
                    title: "Boolpress",
                    content: "Boolpress è una replica di Wordpress, permette infatti all'utente registrato di postare attraverso la propria dashboard nuovi post per il proprio blog, dove ovviamente tutti gli utenti anche non registrati potranno visualizzarli.",
                     badges: ['Vue', 'Laravel', 'Axios', 'Database'] 
                },
                {
                    image: "boolzapp.png",
                    title: "Vue-Boolzapp",
                    content: "Replica dell'app di messagistica, consente di mandare messaggi ai proprio contatti e tramite una funzione JS si riceverà una risposta in automatico da un array di risposte casuali.",
                    badges: ['Vue'] 
                },
                {
                    image: "campo_minato.png",
                    title: "Campo minato",
                    content: "Cerca di vincere il gioco campo minato con 3 livelli di difficoltà, è praticamente impossibile.",
                    badges: ['HTML5', 'CSS', 'Javascript'] 
                },
                {
                    image: "todolist.png",
                    title: "Vue-Todolist",
                    content: "Aggiungi, modifica ed elimina elemnti dalla tua lista in modo semplice e veloce.",
                    badges: ['Vue',] 
                },
                {
                    image: "fizzBuzz.png",
                    title: "FizzBuzz",
                    content: "Laravel-Comics è un negozio di fumetti dove puoi visionare tutti i prodotti disponibili ed entrare nel dettaglio del singolo prodotto.",
                    badges: ['Laravel']
                },
                {
                    image: "palestra.png",
                    title: "Vue-Palestra",
                    content: "Utilizzando Vue ho creato un sito per una palestra dall'aspetto semplice e professionale",
                    badges: ['Vue']
                },
            ]
        };
    },
    
    components: { CardComponent }
}   
</script>

<style scoped>


</style>