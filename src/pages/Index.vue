<template>
  <q-page padding>
    <div class="row">
      <q-input v-model="text" placeholder="Add new task" class="col" />
      <q-btn color="primary" size="sm" label="Add"/>
    </div>
    <div class="row">
        <q-list highlight class="col">
            <q-list-header>Tasks</q-list-header>
            <q-item>
              <q-item-side avatar="statics/linux-avatar.png" />
              <q-item-main label="Jim Doe" />
              <q-item-side right icon="chat_bubble" />
            </q-item>
          </q-list>
    </div>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex'
}
</script>
