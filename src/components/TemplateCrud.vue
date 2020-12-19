<template>
  <AtomHeader :text="title" />
  <MoleculeAddButton :title="buttonTitle"/>
  <AtomSuccessMessage :message="successMessage"/>
  <AtomErrorMessage :message="errorMessage"/>
  <MoleculeGrid :columns="columns" :rows="rows"/>
  <OrganismAddModal :modalTitle="modalTitle" :textButton="modalTitle"/>
</template>

<script>
import AtomHeader from '@/components/AtomHeader'
import MoleculeAddButton from '@/components/MoleculeAddButton'
import AtomSuccessMessage from '@/components/AtomSuccessMessage'
import AtomErrorMessage from '@/components/AtomErrorMessage'
import MoleculeGrid from '@/components/MoleculeGrid'
import OrganismAddModal from '@/components/OrganismAddModal'

export default {
  name: 'TemplateCrud',
  components: {
    AtomHeader,
    MoleculeAddButton,
    AtomSuccessMessage,
    AtomErrorMessage,
    MoleculeGrid,
    OrganismAddModal
  },
    data: () => {
    return {
      title: 'Customers',
      buttonTitle: 'Customer',
      successMessage: 'Customer created successfully',
      errorMessage: 'An error ocurred trying to create a customer',
      showSuccess : true,
      columns: ["Name", "Address", "Phone", "Email", "Age"],
      rows: [
        { name: 'Customer 1', address: 'Test Address 1', phone: '123456', email: 'Hello@world.com', age: 29 },
        { name: 'Customer 2', address: 'Test Address 2', phone: '789456', email: 'Hello@world.com', age: 21 },
        { name: 'Customer 3', address: 'Vue', phone: '54856225', email: 'Hello@world.com', age: 20 }
      ],
      modalTitle: 'Add Customer'
    };
  }
  }
</script>