<template>
  <main>
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button class="new-note">+</button>
      </header>
      <div class="cards-container">
        <div class="card">
          <p class="main-text"></p>
          <p class="date"></p>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup></script>

<style scoped>
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

h1 {
  font-size: 2rem;
  font-weight: 400;
}

.new-note {
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
</style>
