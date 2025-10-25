<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12" md="4">
        <v-card>
          <v-card-title>Total Users</v-card-title>
          <v-card-text>1,245</v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <line-chart />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import LineChart from "@/components/LineChart.vue";

export default {
  components: { LineChart }
};
</script>