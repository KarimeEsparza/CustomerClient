<template>
    <div class="row">
        <div class="col-lg-12">
            <table class="table table-bordered table-striped">
                <thead>
                    <tr class="text-center bg-info text-light">
                        <th v-for="(column, i) in columns" :key="i"> {{ column }}</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(data, i) in rows" :key="i" class="text-center">
                        <AtomGridContent :data="data" />
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<script>

import AtomGridContent from '@/components/AtomGridContent'

export default {
  name: 'MoleculeGrid',
  props: ["columns", "rows"],
  components: {
    AtomGridContent
  }
}
</script>
