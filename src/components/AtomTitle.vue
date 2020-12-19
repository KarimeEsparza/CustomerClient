<template>
     <h3 class="text-info">{{ text }}</h3>
</template>

<script>
export default {
  name: "AtomTitle",
 props: {
    text: String
  }
};
</script>