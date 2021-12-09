<template>

  <q-page padding class="row">
   <!--
    <q-card style="width: 350px;">
      <q-card-section class="bg-red text-white">
        My Card
      </q-card-section>

       <q-card-section>
        This is a card section.
      </q-card-section>
    </q-card>
    -->

    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input borderless dense placeholder="Search" class="full-width"  :model-value="search">
          <template #append>
            <q-icon name="mdi-magnify"></q-icon>
          </template>
        </q-input>
      </q-toolbar>
     
      <TodosList bordered>
        
      </TodosList>
    </q-card>


   

    <!-- <q-btn color="green-10" label="Quasar Button"></q-btn> -->

    <!-- <q-select v-model="selected" label="People" filled :options="['Faggot', 'Whore', 'Bastard', 'My Dick' ]"></q-select> -->
      
    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <CreateTodoButton fab color="secondary" icon="mdi-plus" style="margin-bottom: -42px;" class="q-ml-lg"/>
      </q-toolbar>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import { colors } from 'quasar'
import CreateTodoButton from 'components/CreateTodoButton.vue'
import TodosList from 'components/TodosList.vue'

const { getPaletteColor } = colors
export default defineComponent({
  name: 'PageIndex',

  components: {
    CreateTodoButton,
    TodosList,
  },
  
  data() {
    return {
      selected: '',
    }
  },

  mounted() {
    console.log(getPaletteColor('blue-9'))
  },
  
})
</script>

<style lang="scss">

</style>
