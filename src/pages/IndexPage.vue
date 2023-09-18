<template>
  <q-page padding class="column flex-center">
    <!-- <q-date v-model="selectedDate" /> -->
    <br />
    <div class="q-pa-md" style="max-width: 300px">
      <q-input filled v-model="selectedDate" mask="date" :rules="['date']">
        <q-popup-proxy>
          <q-banner style="padding: 0;">
            <q-date v-model="selectedDate" minimal today-btn>
              <div class="row items-center justify-end">
                <q-btn v-close-popup label="Close" color="primary" flat />
              </div>
            </q-date>
          </q-banner>
        </q-popup-proxy>
        <template v-slot:append>
          <q-icon name="event" class="cursor-pointer" />
        </template>
      </q-input>
      <p style="padding: 0;margin:-15px 0 0 15px;">MM/DD/YYYY</p>
    </div>
  </q-page>
</template>

<script>
import { ref, onMounted } from 'vue'

const selectedDate = ref()
const date = ref('');

</script>