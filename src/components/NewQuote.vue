<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
                <label>Quote</label>
                <textarea name="" id="" cols="80" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
                <button class="btn btn-primary" @click.prevent="createNew">Add quote</button>
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
                this.$emit('quoteAdded', this.quote)
            }
        }
    }
</script>

<style scoped>

    label {
        width: 100%
    }


</style>