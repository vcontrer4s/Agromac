<style>
  .Main {
    display: grid;
    grid-template-columns: minmax(auto, 936px);
    justify-content: center;
    background-color: #fafafa;
  }
  .Main-container {
    display: grid;
    grid-gap: 2em;
    padding: 2em 0;
  }
</style>

<div class="Main">
  <div class="Main-container">
    <slot />
  </div>
</div>
