<template>
  <section class="section">
    <h2 class="title">Lista de Pedidos</h2>
    <div class="columns is-mobile is-multiline">
      <Pedi v-for="pedi in pedis" :key="pedi.id" :pedi="pedi" />
    </div>
  </section>
</template>

<script>
import Pedi from '~/components/Pedi'

export default {
  name: 'HomePage',

  components: {
    Pedi
  },

  data: function() {
    return {
      
    };
  },

  asyncData({ $axios }) {
    return $axios.get("/pedidos/").then(res => {
      return {
        pedis: res.data
      }
    });
  }
};
</script>
