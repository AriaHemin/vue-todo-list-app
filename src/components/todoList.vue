<template>
    <div id="task-add" >
        <input  v-model="text" ><button @click="items.push({title: text, id: id++}), text = ''">add</button>
    </div>
    <div id="task-place">
        <li id="tasks-items" v-for="(item, index) in items" v-bind:key="index">
        <div class="task-itself" > <div>{{item.id}} {{ item.title }}</div> <span><button @click="removeTask(index)"> x</button></span></div>
        </li>   
    </div>
</template>

<script>
export default{
    data() {
        return { 
            items: [],
            text: '',
            id: 0,
        }
    },
    methods: {
        removeTask(index){
            this.items = this.items.filter((task, i) => i != index);
        }
    }
}

</script>

<style>
#tasks-items{        
    list-style: none;
}

#task-place{
    text-align: left;
    margin-inline: 20vw;

}

#task-place button{
    background-color: rgb(255, 185, 185);
    border: 0;
    border-radius: 18px;
}

.task-itself{
    display: flex;
    flex-direction: row;
    justify-content: space-between;

}

#task-add input{
    padding: 1px 5px;
    border-radius: 18px;
    border: solid 1px;
}

#task-add button{
    background-color: white;
    border: solid 1px;
    border-radius: 18px;
}



</style>
