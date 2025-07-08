<template>
    <div>
        <div>
            <h1>Formulario V-MODEL</h1>
        </div>

        <div>
            One-way data binding <br>
            Two-way data binding <br>
            v-model-> formularios
        </div>

        <br><br>

        <div>
            <label>Nome</label> <br>
            <input 
                v-model="name"
                type="text"    
            > <br>
            {{ name }} 
        </div>

        <br><br>

        <div>
            <label>Sportes</label><br>
            <select v-model="sports">
                <option value="">Selecione um esporte...</option>
                <option value="futebol">Futebol</option>
                <option value="basquete">Basquete</option>
                <option value="volei">Volei</option>
            </select>
            <br>
            {{ sports }}
        </div>

        <br><br>

        <div>
            <label>Newsletter</label>
            <input 
                v-model="newsletter"
                type="radio"
                value="yes"
            > 
            Sim

            <input 
                v-model="newsletter"
                type="radio"
                value="no"
            >
            Não <br>

            {{ newsletter }}
        </div>

        <br><br>
        <div>
            <label>Cores que você mais gosta</label>
            <input 
                v-model="colors"
                type="checkbox"
                value="Azul"
            > 
            Azul

            <input 
                v-model="colors"
                type="checkbox"
                value="Branco"
            >
            Branco <br>

            {{ colors }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'TheForm',
    data() {
        return {
            name: 'Jon Snow',
            sports: '',
            newsletter: '',
            colors: []
        }
    }
}
</script>
