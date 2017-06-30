<template>
    <div class="results">
        <div class="container">
            <table class="table">
  <thead>
    <tr>
      <th>page_title</th>
      <th>url</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="result in results">
      <td>{{result.page_title}}</td>
      <td>{{result.url}}</td>
    </tr>
  </tbody>
</table>
        </div>
    </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      results: [
        {
          'id': 1,
          'page_title': 'Bootstrap Vue',
          'url': 'bootstrap-vue.js.org'
        },
        {
          'id': 2,
          'page_title': 'C++ — Википедия',
          'url': 'ru.wikipedia.org/wiki/C%2B%2B'
        }
      ]
    }
  }
}
</script>

<style>

</style>
