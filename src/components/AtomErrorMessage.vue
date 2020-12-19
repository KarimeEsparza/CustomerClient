<template>
    <div id="errorMsg" class="alert alert-danger"  style="display: none">
       <button type="button" class="close" onclick="hideElement('errorMsg')">
        <span aria-hidden="true">&times;</span>
      </button>
        <span id="innerError">{{ message }}</span>
    </div>
</template>

<script>
export default {
  name: "AtomErrorMessage",
 props: {
    message: String
  }
};
</script>