<template>
  <section class="filter-card py-3">
      <select 
      v-model="checkedSearch"
      @change="$emit('checkedCard', checkedSearch)"
      >
      <option value="all">  ALL</option>
      <option value="rock">  ROCK</option>
      <option value="jazz">  JAZZ</option>
      <option value="pop">  POP</option>
      
      </select>
  </section>
</template>

<script>
export default {
    name: "AppFilterCard",
    data: function () {
        return {
            checkedSearch: "all",
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.filter-card {
    display: flex;
    justify-content: center;
    margin: auto;
}

select {
    width: 30%;
    border-radius: 2rem;
    height: 40px;
}

.option {
    margin-left: 10px;
}

</style>