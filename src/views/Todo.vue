<template>
  <div class="home">
    
    <list-tasks 
    v-if="$store.state.tasks.length"
    />
   <no-tasks
    v-else
   />
    <button-done-sorting
    v-if="$store.state.sorting"
    >

    </button-done-sorting>
  </div>
</template>

<script>
export default {
  name: 'Home',
  components:{
    'list-tasks': require('@/components/Todo/ListTasks.vue').default,
    'no-tasks': require('@/components/Todo/NoTask.vue').default,
    'button-done-sorting': require('@/components/Todo/ButtonDoneSorting.vue').default,
  }
}
</script>
