<template>
    <div class="backsdrop" @click.self="closeModal">
        <div class="modal">
            <h1>{{ header }}</h1>
            <p>{{ text }}</p>
        </div>
    </div>
</template>

<script>
export default{
    props: ['header', 'text'],

    methods: {
        closeModal(){
            this.$emit('close')
        }
    }
}
</script>
