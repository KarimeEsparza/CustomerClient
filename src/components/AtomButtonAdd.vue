<template>
     <button class="btn btn-info" onclick="showElement('overlay')">
        <i class="fas fa-user">&nbsp; Add {{ text }}</i>
     </button>
</template>

<style>
  #overlay{
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.6)
  }  
</style>

<script>
export default {
  name: "AtomButtonAdd",
 props: {
    text: String
  }
};
</script>