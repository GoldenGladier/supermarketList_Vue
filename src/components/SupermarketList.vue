<template>
    <section class="section">
        <div class="section"> 
            <b-field label="Supermarket list." class="is-three-quarters">
                <b-input placeholder="Enter the products. Author: Omar Aguirre Alvarez." rounded v-model="textInput"></b-input>
            </b-field>

            <!-- <p>Respuesta: {{ reply() }}</p> -->
            <div v-if="items.length > 0" class="section">
                <ol class="ol">
                    <li v-for="item in items" :key="item.id">
                        {{ item.name }}: {{ item.number }}
                    </li>
                </ol>  
            </div>
        </div>      
    </section>
</template>

<script>
export default {
    name: "SupermarketList",
    data(){
        return{
            text: "",   
            items: []
        };
    },
    methods: {
        cortar: function(){
            this.items = [];
            var words = this.text.split(',');             
            words.forEach((element) => {
                var parts = [];
                parts = element.trim().split(' ');
                if(parts[0] && parts[1]){
                    this.items.push({
                        name: parts[0],
                        number: parts[1]
                    });
                }                
            });
        }
    },
    computed: {
        textInput: {
            get(){
                return this.text;
            },
            set(newText){
                this.text = newText;
                this.cortar();
            },
        },        
    },
}
</script>