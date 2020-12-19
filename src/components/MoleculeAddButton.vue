<template>
    <div class="container">
        <div class="row mt-3">
            <div class="col-lg-6">
                <AtomTitle :text="title"/>
            </div>
            <div class="col-lg-6 d-flex justify-content-end">
                <AtomButtonAdd :text="title"/>
            </div>
        </div>
        <hr class="bg-info">
    </div>
</template>

<script>
import AtomTitle from '@/components/AtomTitle'
import AtomButtonAdd from '@/components/AtomButtonAdd'

export default {
  name: 'MoleculeAddButton',
  components: {
    AtomTitle,
    AtomButtonAdd
  },
  props: {
      title: String
  }
}
</script>