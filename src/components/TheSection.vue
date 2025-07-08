<template>
    <div>
        <h1 :class="{ 'title': true, 'title-home': isHome }">
            Curso VUE 3
        </h1>

        <p :class="['text', 'title']">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Molestiae expedita odit dicta sapiente, quas perspiciatis veritatis iure explicabo cupiditate. Eos praesentium quasi, quos natus sint iure nulla quas eaque saepe!
        </p>

        <p :style="{ 'color': 'blueviolet'}">
            lipsum dolor sit amet consectetur adipisicing elit. Molestiae expedita odit dicta sapiente, quas perspiciatis veritatis iure explicabo cupiditate. Eos praesentium quasi, quos natus sint iure nulla quas eaque saepe!
        </p>

        <div 
            v-for="(obj, index) in todos" 
            :key="obj.id" 
            class="todos-item"
        >
            <img 
                v-if="obj.imgSrc"
                :src="obj.imgSrc" 
            
            />
            {{ index }} - {{ obj.title }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'TheSection',
    data() {
        return {
            isHome: false,
            classVar: 'title',
            pClass: 'text',
            todos: [
                {
                    "userId": 1,
                    "id": 1,
                    "title": "delectus aut autem",
                    "completed": false,
                    "imgSrc": "https://placehold.co/150x150/png"
                },
                {
                    "userId": 1,
                    "id": 2,
                    "title": "quis ut nam facilis et officia qui",
                    "completed": false,
                    "imgSrc": "https://placehold.co/150x150/png"
                },
                {
                    "userId": 1,
                    "id": 3,
                    "title": "fugiat veniam minus",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 4,
                    "title": "et porro tempora",
                    "completed": true
                },
                {
                    "userId": 1,
                    "id": 5,
                    "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                    "completed": false
                }
            ]
        }
    }
}
</script>

<style>
.title{
    font-size: 20;
    color: blue;
}

.title-home {
    font-size: 40px;
    color: green;
}

.text {
    color: red;
}

.todos-item {
    background: #000;
    margin: 0 0 5px 0;
    padding: 3px 6px;
    color: #fff;
}
</style>