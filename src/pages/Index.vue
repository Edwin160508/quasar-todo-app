<template>
  <q-page padding>
    <div class="row">
      <q-input v-model="newTask" placeholder="Add new task" class="col" @keyup.enter="addTask" />
      <q-btn color="primary" size="sm" label="Add" @click.native="addTask" />
    </div>
    <div class="row">
        <q-list highlight class="col">
            <q-list-header>Tasks</q-list-header>
            <q-item v-for="(task, index) in tasks" :key="index">
              <q-item-main :label="task" />
              <q-item-side right icon="check" color="green" />
            </q-item>
          </q-list>
    </div>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex',
  data () {
    return { tasks: [], newTask: '' }
  },
  methods: {
    addTask () {
      if (this.newTask !== '') {
        this.tasks.push(this.newTask)
      }
      this.newTask = ''
    }
  }
}
</script>
