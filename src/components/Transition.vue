<template>
    <div>
        <h1>Ex. aula:</h1>
        <button @click="ativo = !ativo">Ativar</button>
        <transition name="fade" @enter="enter" @leave="leave">
        <!-- appear enter-active-class="animar" enter-to-class="animou" -->
        <h1 v-if="ativo">Serviços</h1>
        </transition>
    </div>
</template>

<script>

export default {
    data() {
        return {
        ativo: false
        }
    },
    methods: {
        enter(elemento) {
            console.log(elemento.classList.add("teste"))
        },
        leave() {
            console.log("elemento sumiu")
        }
    }
}

</script>

<style>
.fade-enter-active,
.fade-leave-active {
    transition: opacity 2s;
}

/* .animar {
    transition: opacity 2s;
} */

.fade-enter,
.fade-leave-to {
    opacity: 0;
}
</style>
