<template>
    <div class="container">
        <div class="col-12 text-center">
            <h1>Add Notes VueJs App</h1>
            <img src="./assets/logo.png">
        </div>
        <appHeader :quoteCount="quotes.length" :maxQuotes="maxQuotes"></appHeader>
        <appNewQuote @quoteAdded="newQuote"></appNewQuote>   
        <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote" ></app-quote-grid>
        <div class="row">
            <div class="col-12 text-center">
                    <div class="alert alert-info">Info: Click on the quote to delete it !</div>
            </div>
        </div>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue'
    import newQuote from './components/NewQuote.vue'
    import Header from './components/Header.vue'
    
    export default {
        data: function(){
            return {
                quotes: ['Add a Quote to see the code working'],
                maxQuotes: 10
            }
        },
        methods: {
            newQuote(quote) {
                    if (this.quotes.length >= this.maxQuotes) {
                        return alert ('Please remove Quotes first!')
                    }
                    this.quotes.push(quote);
            },
            deleteQuote(index){
                    this.quotes.splice(index,1);
            }
        },
        
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: newQuote,
            appHeader: Header
        }


        
    }
</script>

<style>

</style>
