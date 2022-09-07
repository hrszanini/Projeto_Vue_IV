<template>
    <div class="usuario">

        <p>
            <input type="text" v-model="name">
            <input type="button" value="OK" @click="inserirUsuario()">
        </p>

        <ui v-if="usuarios.length > 0">
            <li v-for="usuario in usuarios" :key="usuario">
                {{usuario}}
            </li>
        </ui>

    </div>
</template>

<script>
export default {
    data() {
        return {
            name : "Hamilton",
            usuarios : []
        }
    },
    methods: {
        inserirUsuario() {
            if(this.name != ""){
                this.usuarios.push(this.name);
                this.name = "";
            }
        }
    }
}
</script>