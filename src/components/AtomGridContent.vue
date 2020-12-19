<template>
    <td v-for="(field, i) in data" :key="i">{{ field }}</td>
</template>

<script>
export default {
  name: "AtomGridContent",
 props: ["data"]
};
</script>