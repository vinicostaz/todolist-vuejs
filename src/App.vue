<template>
  <div id="app">
     <b-navbar toggleable="lg" type="dark" variant="dark">
    <b-navbar-brand href="#">ToDoList</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#">Tarefas</b-nav-item>
        <b-nav-item href="#">Formulário</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<style>

</style>