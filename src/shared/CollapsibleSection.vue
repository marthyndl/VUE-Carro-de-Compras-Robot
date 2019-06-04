<template>
    <div>
        <div class="header">
            <span v-if="open" @click="open = !open" >&#x25B2; Cerrar</span>
            <span v-if="!open" @click="open = !open">&#x25BC; Expandir</span>
        </div>
        <!-- Toggleable -->
        <slot v-if="open">
            <div>defaultContent</div>
        </slot>
    </div>
</template>

<script>
export default {
    name: 'CollapsibleSection',
    data() {
        return {
            open: true,
        }
    }
}    
</script>

<style scoped>
.header {
    background-color: #bbb;
    padding: 3px;
    cursor: pointer;
}
</style>
