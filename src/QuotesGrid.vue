<template>
    <div class="row">
        <app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{quote}}</app-quote>

    </div>
</template>

<script>
import Quotes from './Quotes.vue'

export default {
    props: ['quotes'],
    
    components:{
        'app-quote': Quotes
    },
    methods:{
        deleteQuote(index){
            this.$emit('quoteDeleted' , index);

        }
    }
}
</script>

<style>

</style>