<template>
  <div class="container mt-2">
    <b-form>
      <b-form-group
        label="Titulo"
        label-for="subject"
      >
      <b-form-input
        id="subject"
        v-model="form.subject"
        type="text"
        placeholder="Ex: Lavar carro"
        required
        autocomplete="off"
      ></b-form-input>
    </b-form-group>

    <b-form-group
        label="Descrição"
        label-for="description"
      >
      <b-form-textarea
        id="description"
        v-model="form.description"
        type="text"
        placeholder="Ex: Preciso levar o carro para lavar"
        required
        autocomplete="off"
      ></b-form-textarea>
    </b-form-group>
    <b-button
    type="submit" variant="outline-primary" @click="saveTask"> Salvar </b-button>
  </b-form>
</div>
</template>

<script>
export default {
  name: "Form",

  data() {
    return {
      form: {
        subject: "",
        description: ""
      }
    }
  },

    methods: {
      saveTask() {
        let tasks = (localStorage.getItem("tasks")) ? JSON.parse(localStorage.getItem("tasks")) : [];
        tasks.push(this.form);
        localStorage.setItem("tasks", JSON.stringify(tasks));
        this.$router.push({ name: "list" })
    }
  }
}
</script>