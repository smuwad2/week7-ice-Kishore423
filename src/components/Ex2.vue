<script>


    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
            }
            
        },
        methods: {
            deleteItem(idx){
                this.items.splice(idx, 1) //remove 1 item at given index, idx 
            },
            AddItem(){
                this.items.push(this.something)
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for="(item,idx) in items" >
            {{ item }}
            <button @click=deleteItem(idx)>Delete!</button>


        </li>
     </ul>

     <input  v-model="something"></input><button @click='AddItem(something)'>Add!</button>
     

   
</template>
