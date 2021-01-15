<template>
  <div class="column is-full-mobile is-half-tablet is-one-third-desktop is-one-quarter-widescreeen">
    <div class="card">
      <header class="card-header">
        <p class="card-header-title">
          Pedido Nº: {{ pedi.pedido_id}}
        </p>
      </header>
      <div class="card-body" @click="isModalActive=true">
        <h3 style="text-align:center">
          {{ pedi.status }}
        </h3>
      </div>
      <footer class="card-footer">
        <a class="button is-light card-footer-item">
          <b-icon v-if="pedi.status !== 'PROCESO'" icon="hand-okay"></b-icon>
          <p v-if="pedi.status === 'PROCESO'">
            Pedido pendiente de elaboración
          </p>
        </a>
      </footer>
      <!-- Modal para los datos del pedido -->
      <b-modal :active.sync="isModalActive">
        <div class="card">
          <div class="card-content">
            <h2 class=title>
              Pedido Nº {{ pedi.pedido_id }}
            </h2>
            <h3>
              Cliente: {{ pedi.cliente }}
            </h3>
            <h3>
              Platos: {{ pedi.nombre }}
            </h3>
            <h3>
              Estado del pedido: {{ pedi.status }}
            </h3>
          </div>
        </div>
      </b-modal>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    pedi: {
      type: Object
    }
  },
  data() {
    return {
      isModalActive: false
    }
  }
}
</script>

<style>
.card-body,
.modal-background {
  cursor: pointer !important;
}

.card-body {
  background-color: #edcbb1;
}
</style>
