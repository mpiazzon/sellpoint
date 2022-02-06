<template>
  <v-row class="pa-6">
    <v-col cols="12" md="8">
      <v-text-field
        v-model="message1"
        label="codigo de barras"
        clearable
      ></v-text-field>
      <v-btn>buscar</v-btn>
      <v-btn>agregar generico</v-btn>
      <v-text-field type="number" label="cantidad"></v-text-field>
      <v-table fixed-header height="300px">
        <thead>
          <tr>
            <th class="text-left">codigo</th>
            <th class="text-left">descripcion</th>
            <th class="text-left">cantidad</th>
            <th class="text-left">precio</th>
            <th class="text-left">total</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in desserts" :key="item.name">
            <td>{{ item.name }}</td>
            <td>{{ item.calories }}</td>
          </tr>
        </tbody>
      </v-table>
    </v-col>
    <v-col cols="4" md="4">
      <v-card color="#222222" theme="dark">
        <v-card-title class="text-h5">Total</v-card-title>

        <v-card-subtitle>$ 4545,00</v-card-subtitle>

        <v-card-actions> </v-card-actions>
      </v-card>
      <v-btn class="my-5" size="x-large" block color="success"
        >imprimir y guardar
      </v-btn>
      <v-btn size="x-large" block color="success">guardar </v-btn>
      <v-btn class="mt-5" size="x-large" block color="grey">cancelar </v-btn>
    </v-col>
  </v-row>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  data() {
    return {
      desserts: [
        {
          name: "Frozen Yogurt",
          calories: 159,
        },
        {
          name: "Ice cream sandwich",
          calories: 237,
        },
        {
          name: "Eclair",
          calories: 262,
        },
        {
          name: "Cupcake",
          calories: 305,
        },
        {
          name: "Gingerbread",
          calories: 356,
        },
        {
          name: "Jelly bean",
          calories: 375,
        },
        {
          name: "Lollipop",
          calories: 392,
        },
        {
          name: "Honeycomb",
          calories: 408,
        },
        {
          name: "Donut",
          calories: 452,
        },
        {
          name: "KitKat",
          calories: 518,
        },
      ],
    };
  },
};
</script>
