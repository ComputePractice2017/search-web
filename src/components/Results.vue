<template>
  <div class="results">
    <div class="logo">
    <img src="https://pp.userapi.com/c841328/v841328106/4785/AGH_PNmeyes.jpg" alt="1" width="60%" height="90%">
    </div>
    <div class="container">
      <form>
        <div class="form-group">
          <input v-model="message" placeholder="Введите запрос" size="70">
          <button type="button" class="btn btn-primary btn-sm">Поиск</button>
          <br><br><br><br><br><br>
          <b>ИАТЭ НИЯУ МИФИ</b>
          <br>
          <b>Практика 2017</b>
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
.results{
  position: relative;
}
label{
  font-size: large;
}
.logo{
  padding: 2%;
  text-align: center;
}
.container{
  text-align: center;
}
</style>
