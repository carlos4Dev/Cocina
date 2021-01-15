<template background-color="green">
  <div>
    <nav
      class="navbar header has-shadow is-primary"
      role="navigation"
      aria-label="main navigation"
      
    >
      <div class="navbar-brand">
        <a
          class="navbar-item"
          href="/"
        >
          Cocina BitBrasas
        </a>

        <div class="navbar-burger">
          <span />
          <span />
          <span />
        </div>
      </div>
    </nav>

    <section class="main-content columns">
      <aside class="column is-3 section">
        <!--3 en lugar de 2 y 9 por 10 -->
        <p class="menu-label is-hidden-touch">General</p>
        <ul class="menu-list">
          <li>
            <nuxt-link to="/" exact-active-class="is-active">
              <b-icon icon="chef-hat" />Pedidos
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/terminados" exact-active-class="is-active">
              <b-icon icon="hand-okay" />Ayuda
            </nuxt-link>
          </li>
        </ul>
      </aside>

      <div class="container column is-9">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
      
    }
  }
}
</script>
