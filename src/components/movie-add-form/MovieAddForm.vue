<template>
  <div class="movie-add-form">
    <h3>Yangi kino qoshish</h3>
    <form class="add-form d-flex">
      <input
        type="text"
        class="form-control new-movie-label"
        placeholder="Qanday kino? "
        :value="name"
        @:input="name = $event.target.value"
      />
      <input
        type="text"
        class="form-control new-movie-label"
        placeholder="Nechi marotaba ko'rilagan?"
        :value="viewers"
        @:input="viewers = $event.target.value"
      />

      <button class="btn btn-outline-dark" type="submit" @click="addMovie">
        Qo'shish
      </button>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: "",
        viewers: "",
      };
    },

    methods: {
      addMovie() {
        const newMovie = {
          name: this.name,
          viewers: this.viewers,
          favourite: false,
          like: false,
        };
        console.log(newMovie);
      },
    },
  };
</script>

<style>
  .movie-add-form {
    margin-top: 2rem;
    padding: 1.5rem;
    border-radius: 4px;
    background-color: #fcfaf5;
    box-shadow: 15px 15px 15px rgb(0, 0, 0, 0.15);
  }
</style>
