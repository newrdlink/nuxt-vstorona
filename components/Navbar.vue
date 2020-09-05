<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <nuxt-link class="navbar-brand" to="#">NuxtJS</nuxt-link>
      <div class="collapse navbar-collapse">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <nuxt-link class="nav-link" to="/"
              >Home <span class="sr-only">(current)</span></nuxt-link
            >
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/features">Features</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/users">Users</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/about">About</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link
              class="nav-link disabled"
              to="#"
              tabindex="-1"
              aria-disabled="true"
              >Disabled</nuxt-link
            >
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>
