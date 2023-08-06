<template>
    <div>
        <ul>
            <li v-for="(todoItem, index) in propsdata" :key="todoItem.item" class="shadow">
            <i class="checkBtn fa-solid fa-check" @click="toggleComplete(todoItem, index)" :class="{checkBtnCompleted: todoItem.completed}"></i>
            <span :class="{textCompleted: todoItem.completed}">{{ todoItem.item }}</span>
            <span @click="removeTodo(todoItem, index)" class="removeBtn">
                <i class="fa-solid fa-trash-can"></i>
            </span>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    props: ['propsdata'],
    data: function() {
        return {

        }
    },
    methods: {
        removeTodo: function(todoItem, index){
            this.$emit('removeItem', todoItem, index);
        },
        toggleComplete: function(todoItem,index) {
            this.$emit('toggleItem', todoItem, index);
        }
    },  
    
}
</script>
<style scoped>
    ul {
        list-style-type: none;
        padding-left: 0px;
        margin-top: 0;
        text-align: left;
    }
    li {
        display: flex;
        min-height: 50px;
        height: 50px;
        line-height: 50px;
        margin: 0.5rem 0;
        padding: 0 0.9rem;
        background: white;
        border-radius: 5px;
    }
    .checkBtn {
        line-height: 45px;
        color: #62acde;
        margin-right: 5px;
    }
    .checkBtnCompleted {
        color: #b3adad;
    }
    .textCompleted {
        text-decoration: line-through;
        color: #b3adad;
    }
    .removeBtn {
        margin-left: auto;
        color: #de4343;
    }
</style>