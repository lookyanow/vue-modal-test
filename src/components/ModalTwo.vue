<template>
    <div class="backsdrop" @click="closeModal">
        <div class="modal">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default{
    // props: ['header', 'text'],

    methods: {
        closeModal(){
            this.$emit('close')
        }
    }
}
</script>
