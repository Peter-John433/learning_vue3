<template>
    <div>
        <div class="myclass">
            learning class binding and style binding
        </div>
        <div>
            <div>
                <div 
                    :style="{backgroundColor : bg, color: color, 'font-size' : fs + 'px'}" 
                    :class="{ active : isActive, notActive : hasErr }">
                    What is Lorem Ipsum?
                </div>
                <div 
                     :style="myStyleObj"
                    :class="myClassObj">
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
  import { ref, computed } from 'vue';

  const isActive = ref(true);
  const hasErr = ref(false);

  const myClassObj = ref({
      isActive : true,
      noActive: false,
  })

  const color = ref('red');
  const bg = ref('green');
  const fs = ref(20);

  const myStyleObj = ref({
      color : 'black',
      backgroundColor : 'green',
      fontSize: 15 + 'px',
      padding: 10 + 'px',
      width : '400px',
  });
</script>
