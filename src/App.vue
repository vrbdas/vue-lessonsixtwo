<script setup>
import AppBlock from './components/AppBlock.vue';
</script>

<template>
  <main>
    <div class="container">
      <section class="slots">
        <h1 slots__title>Slots</h1>
        <div class="slots__card">
          <app-block>

            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Modi dolorem non esse mollitia animi
              similique culpa consectetur corrupti repellat ad quo aut, cupiditate perferendis accusantium laboriosam?
              Perspiciatis sunt quidem voluptatem?</p>

            <template v-slot:header>
              <h3>This is header</h3>
            </template>

            <template v-slot:footer>
              <hr>
              <h3 class="small">Footer footer footer footer</h3>
            </template>
          </app-block>
        </div>
      </section>
    </div>
  </main>

</template>

<style scoped lang="scss">
$first: #fff;
$second: #FF9F1C;
$third: #FFBF69;
$fourth: #CBF3F0;
$fifth: #2EC4B6;

main {
  height: 100vh;
  background-color: $fourth;
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

  &__title {
    font-weight: 800;
    font-size: 2rem;
  }

  &__card {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
    background-color: $first;
    border-radius: 10px;
    padding: 20px;
  }
}

.small {
  font-size: 0.8rem;
}
</style>
