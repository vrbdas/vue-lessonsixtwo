<script setup>
import AppBlock from './components/AppBlock.vue';
import AppList from './components/AppList.vue';
</script>

<template>
  <main>
    <div class="container">
      <section class="slots">
        <div class="card">
          <h1 class="title">Slots</h1>
        </div>
        <app-block>
          <template v-slot:footer>
            <hr>
            <small>footer footer footer</small>
          </template>
          <template v-slot:default>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea neque nisi aspernatur iste fugiat ipsam magni laboriosam recusandae sapiente consequuntur ex a, laudantium eos debitis labore possimus totam sit voluptates.</p>
          </template>
          <template #header>This is header</template>
        </app-block>
        <app-list>
          <template #default="{idx, iter}">
            <span class="darkred">{{ idx }} {{ iter }}</span>
          </template>
        </app-list>
      </section>
    </div>
  </main>
</template>

<style scoped lang="scss">
main {
  background-color: #CBF3F0;
  padding: 40px 0;
}

.container {
  width: 1320px;
  margin: 0 auto;
}

.slots {
  width: 600px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.title {
    font-weight: 800;
    font-size: 2rem;
  }

.card {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  background-color: #ffffff;
  border-radius: 10px;
  padding: 20px;
}
.darkred {
  color: darkred;
}
</style>
