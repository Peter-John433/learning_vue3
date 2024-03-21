<template>
    <div>
        <div :style="myStyle">
            conditional statement (v-if, v-elsw-if, v-else and v-show)
        </div>

        <div>
            <button @click="ToggleMe">
                <span v-if="showMe">hideMe</span>
                <span v-else>showMe</span>
            </button>
            <div v-if="showMe"
                 :style="myStyleObj"
            >   
                v-if
                Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
            </div>
            <div 
                v-else
                :style="myStyleObj"
            >
                 v-else
                Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap 
            </div>
        </div>
       
    </div>
</template>

<script setup>
 import { ref } from 'vue';

 const myStyle = ref({
     color : 'white',
     backgroundColor : 'green',
     padding : '20px',
     textAlign : 'center',
     fontSize : 20 + 'px',
     textTransform : 'capitalize'
 });

 const myStyleObj = ref({
      color : 'black',
      backgroundColor : 'green',
      fontSize: 15 + 'px',
      padding: 10 + 'px',
      width : '400px',
      margin: 'auto'
  });

 const showMe = ref(true);

 const ToggleMe = () =>{
     showMe.value = !showMe.value;
 }
 
</script>
