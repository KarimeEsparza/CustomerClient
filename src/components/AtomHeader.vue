<template>
    <div class="container-fluid">
        <div class="row bg-dark">
            <div class="col-lg-12">
                <p class="text-center text-light display-6">{{ text }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'AtomHeader',
  props: {
    text: String
  }
}
</script>