<!-- <script>
export default {
    data() {
        return{
            itemName: '',
           arr : []
        }
       

    },
    methods: {
       
addItem(){
console.log('works')
if(!this.input) return;

this.arr.push(this.input)

this.input=''

this.$refs.input.focus()

}
    }
}
</script> -->
<script setup>
import { ref, reactive } from 'vue';

const input = ref('')


const arr = ref([])

// const listItem = reactive({
//     itemName:''
// })
function addItem() {
    if (input.length < 1) {
        input.value = ''
        input.value.focus()

    } else {
        arr.value.push(input.value)
        input.value = ''
        input.value.focus()
    }
}
function delItem(i){
arr.value.splice(i,1)
}

function deleteAll(){
    arr.value = []
}
</script>


<template>
    <h1>
        Shoping List
    </h1>
    <div class="form">
        <input type="text" placeholder="Press Enter to add new item " v-model="input" class="input"
            @keyup.enter="addItem" />
        <button @click="addItem" class="btn" type="submit">
            Add Item
        </button>

    </div>
    <div class="box">
        <!-- <p>{{ input }}</p> -->

        <ol>
            <li v-for="(i, index) in arr" :key="index" class="list">
                <!-- {{ arr }} -->
                {{ i }}
                <button @click="delItem(index)" class="btn-remove">
                    Remove
                </button>
            </li>
        </ol>
    </div>
    <button class="btnDel" @click="deleteAll">Delete All</button>
</template>
<style>
.form {
    display: flex;
    flex-direction: row;
    /* justify-content: space-between; */

}

.btn {
    margin-left: 15px;
    border-radius: 10px;
    width: 85px;
    background-color: rgb(2, 2, 61);
    color: white;
    border: none;
}

.input {
    border-radius: 2px;
    width: 450px;
    height: 35px;
    /* border: none; */
}

.box {
    /* border-style: solid; */
    /* border: 10px; */
    margin-top: 20px;
    border: solid thin black;

}

.btnDel {
    background-color: red;
    color: white;
    border-radius: 10px;
    width: 100px;
    height: 35px;
    margin-top: 20px;
    border: none;
}
.btn-remove{
color: red;
border: none;
margin-left: 350px;
background-color: white;
}
/* .order{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
} */
.list{
margin-top: 10px;
margin-bottom: 10px;
}
</style>