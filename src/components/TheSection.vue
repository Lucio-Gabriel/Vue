<template>
    <div>
        <div 
            v-for="(obj, index) in todos" 
            v-bind:key="obj.id" 
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
.todos-item {
    background: #000;
    margin: 0 0 5px 0;
    padding: 3px 6px;
    color: #fff;
}
</style>