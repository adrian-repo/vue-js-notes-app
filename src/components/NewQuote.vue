<template>
    <div class="row">
        <form>
            <div class="col-12 form-group text-center">
                <h2>Quote</h2>
                <textarea id="newQuote" cols=100% rows="2" v-model="quote"></textarea>
            </div>
            <div class="col-2 form-group text-center">
                <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>    
</template>


<script>
export default {
    data: function() {
        return {
            quote: ''
        }
    },

    methods: {
        createNew() {
                this.$emit('quoteAdded', this.quote);
                this.quote='';

        }

    }
    
}
</script>

<style>

</style>


