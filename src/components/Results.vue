<template>
  <div class="results">
    <div class="container">
      <form>
        <div class="form-group">
          <label for="exampleInputEmail1">Поисковая страница</label>
          <br>
          <input v-model="message" placeholder="Введите запрос" size="100">
          <button type="button" class="btn btn-primary btn-sm">Поиск</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>

</script>

<style>
input{

  border: 2px groove #B9B9BC;
}
button{
  height: 30px;
}
</style>
