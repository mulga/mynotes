<script setup>
import { ref } from "vue";
const showModal = ref(false);

//
</script>

<template>
  <main>
    <div v-if="showModal" class="overlay">
      <div class="modal">
        <textarea name="newNote" id="newNote" cols="30" rows="10"></textarea>
        <button class="btn-add-note">Add Note</button>
        <button @click="showModal = false" class="btn-close">Close</button>
      </div>
    </div>
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button @click="showModal = true" class="btn-new-note">+</button>
      </header>
      <div class="cards-container">
        <div class="card">
          <p class="main-text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur,
            praesentium?
          </p>
          <p class="date">12.05.2022</p>
        </div>
        <div class="card">
          <p class="main-text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur,
            praesentium?
          </p>
          <p class="date">12.05.2022</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
.overlay {
  position: absolute;
  z-index: 99;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.3);
  display: flex;
  align-items: center;
  justify-content: center;
}

main {
  height: 100vh;
  width: 100vw;
}
.container {
  max-width: 1000px;
  padding: 10px;
  margin: 0 auto;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
}

h1 {
  font-size: 2rem;
  font-weight: 400;
}

.btn-new-note {
  font-size: 2rem;
  font-weight: 400;
  padding: 1rem;
  width: 3rem;
  height: 3rem;
  border: none;
  border-radius: 50%;
  background: #cccc;
  cursor: pointer;
  display: grid;
  place-content: center;
}

.card {
  width: 250px;
  height: 250px;
  background: #cccc;
  padding: 0.8rem;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 0.8rem;
}

/* model */

.modal {
  width: 750px;
  background-color: #fff;
  border-radius: 10px;
  padding: 2rem;
  position: relative;
  display: flex;
  flex-direction: column;
}

.btn-add-note,
.btn-close {
  padding: 0.8rem 1rem;
  border: none;
  background-color: green;
  color: #fff;
  font-size: 1.1rem;
  margin-top: 1rem;
}
.btn-close {
  background-color: red;
}
</style>
