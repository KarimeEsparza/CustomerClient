<template>
    <div id="successMsg" class="alert alert-success" style="display: none">
      <button type="button" class="close" onclick="hideElement('successMsg')">
          <span aria-hidden="true">&times;</span>
        </button>
        <span>{{ message }}</span>
    </div>
</template>

<script>
export default {
  name: "AtomSuccessMessage",
 props: {
    message: String
  }
};
</script>