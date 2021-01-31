<template>
    <div>        
    <button :class="{red: hasError, green: green, pink: pink, blue: blue}" >{{ title }}</button>
    <p v-if="error">{{ error }}</p>
    </div>

</template>

<script>
export default {
    name:"Bouton",
    props:  {
        title:  {
            type: String,
            required: true
        },
        hasError: {
            type: Boolean,
            required: false,
        },
        error: {
            type: String,
            required: false
        },
        green: {
            type: Boolean,
            required: true
        },
        pink: {
            type: Boolean,
            required: true
        },
        blue: {
            type: Boolean,
            required: true
        }
    },
}
            

</script>

<style>
.red {
    border: red 1px solid;
}

.green {
    background: green;
    color: white;
}

.pink {
    background: rgb(192, 10, 162);    
    border: blue 2px solid;
    border-radius: 50px;
    color:black;
    /*filter: blur(4px); */
}

.blue {
    background: blue;
    color: white;

}
    


</style>
