<template>
    <input :type="type" />
</template>

<script>
export default {
  name: "AtomField",
 props: {
    type: String
  }
};
</script>