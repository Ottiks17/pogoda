<script>
import WelcomeItem from './WelcomeItem.vue';

export default {
  name: "parent",
  component: {WelcomeItem,},

  
};

</script>

<template>
 <div class="parent">
  <WelcomeItem>
    <p>Hi</p>
  </WelcomeItem>
 </div>
</template>
