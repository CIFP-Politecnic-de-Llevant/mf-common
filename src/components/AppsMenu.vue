<template>
  <q-btn color="grey" label="Apps">
    <q-menu>
      <q-list style="min-width: 100px">
        <q-item v-if="appUsuarisEnabled" clickable v-close-popup :href="appUsuarisURL">
          <q-item-section>Usuaris</q-item-section>
        </q-item>
      </q-list>
    </q-menu>
  </q-btn>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import { Todo, Meta } from './models';

export default defineComponent({
  name: 'ExampleComponent',

  data(){
    return {
      appUsuarisEnabled: process.env.APP_ENABLE_USUARIS,
      appUsuarisURL: process.env.APP_URL_USUARIS
    }
  },
  methods: {

  }
});
</script>
