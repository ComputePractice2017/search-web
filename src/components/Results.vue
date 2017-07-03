<template>
  <div class="results">
    <!-- картинка -->
    <div class="logo">
    <img src="https://pp.userapi.com/c841328/v841328106/4785/AGH_PNmeyes.jpg" alt="1" width="60%" height="90%">
    </div>
    <div class="container">
      <form>
        <!-- Главная страница -->
        <div class="form-group">
          <form class="form-wrapper">
            <input id="search" placeholder="Введите запрос ..." required="" type="text" v-model="search">
            <input  type="submit" id="submit" value="Поиск">
          </form>
          <br><br><br><br><br><br><br>
          <H1>ИАТЭ НИЯУ МИФИ</H1>
          <H1><font size="2">Практика 2017</font></H1>
        </div>
        <!-- Страница с результатами -->
        <div>

        </div>    
      </form>
    </div>
  </div>
</template>

<script>

  export default {
    data () {
      return {
        // Список результатов
        resultslist: [
          {
            'id': 1,
            'name': 'Программирование — Википедия',
            'url': 'ru.wikipedia.org/wiki/Программирование'
          },
          {
            'id': 2,
            'name': 'Что такое программирование? Программирование для...',
            'url': 'fb.ru/article/174427/chto-takoe-programmirovanie-programmirovanie-dlya-nachinayuschih'
          },
          {
            'id': 3,
            'name': 'Основы программирования - курс для начинающих...',
            'url': 'codingcraft.ru/programming_for_beginners.php'
          }
        ],
        edit: false,
        search: ''
      }
    },

    /* проверка строки на пустоту */
    computed: {
      container: function () {
        var search = this.search
        if (this.search !== '') {
          return '' /* нужно удалить картинку и загрузить результаты */
        }
      }
    }
  }

</script>

<style>

.logo{
  padding: 2%;
  text-align: center;
}

.container{
  text-align: center;
}

/*Задаем общий вид формы. Добавляем тень, границу и создается эффект объема*/
.form-wrapper {
    width: 600px;
    padding: 8px;
    margin: 10px auto; 
    overflow: hidden;
    border-width: 1px;
    border-style: solid;
    border-color: #dedede #bababa #aaa #bababa;
    -moz-box-shadow: 0 3px 3px rgba(255,255,255,.1), 0 3px 0 #bbb, 0 4px 0 #aaa, 0 5px 5px #444;
    -webkit-box-shadow: 0 3px 3px rgba(255,255,255,.1), 0 3px 0 #bbb, 0 4px 0 #aaa, 0 5px 5px #444;
    box-shadow: 0 3px 3px rgba(255,255,255,.1), 0 3px 0 #bbb, 0 4px 0 #aaa, 0 5px 5px #444;
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    border-radius: 10px;    
    background-color: #f6f6f6;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#f6f6f6), to(#eae8e8)); 
    background-image: -webkit-linear-gradient(top, #f6f6f6, #eae8e8);
    background-image: -moz-linear-gradient(top, #f6f6f6, #eae8e8);
    background-image: -ms-linear-gradient(top, #f6f6f6, #eae8e8);
    background-image: -o-linear-gradient(top, #f6f6f6, #eae8e8);
    background-image: linear-gradient(top, #f6f6f6, #eae8e8);
}

/*задаем стили для поля ввода когда оно неактивно*/
.form-wrapper #search {
    width: 460px;
    height: 30px; /*20*/
    padding: 10px 5px;
    float: left;    
    font: lighter 16px 'lucida sans', 'trebuchet MS', 'Areal'; /*стиль текста в строке*/
    border: 1px solid #ccc;
    -moz-box-shadow: 0 1px 1px #ddd inset, 0 1px 0 #fff;
    -webkit-box-shadow: 0 1px 1px #ddd inset, 0 1px 0 #fff;
    box-shadow: 0 1px 1px #ddd inset, 0 1px 0 #fff;
    -moz-border-radius: 3px;
    -webkit-border-radius: 3px;
    border-radius: 3px;      
}

/*задаем стили для поля ввода когда оно в фокусе, т.е. когда мы набираем текст*/ 
.form-wrapper #search:focus {
    outline: 0; 
    border-color: #aaa;
    -moz-box-shadow: 0 1px 1px #bbb inset;
    -webkit-box-shadow: 0 1px 1px #bbb inset;
    box-shadow: 0 1px 1px #bbb inset;  
}

/*прописываем стили для текста, который находится на фоне*/
.form-wrapper #search::-webkit-input-placeholder {
    color: #999;
    font-weight: normal;
}
 
.form-wrapper #search:-moz-placeholder {
    color: #999;
    font-weight: normal;
}
 
.form-wrapper #search:-ms-input-placeholder {
    color: #999;
    font-weight: normal;
}

/*добавляем стили кнопке поиска*/
.form-wrapper #submit {
    float: right;    
    border: 1px solid #00748f;
    height: 30px; /*42*/
    width: 100px;
    padding: 0;
    cursor: pointer;
    font: bold 15px Arial, Helvetica;
    color: #fafafa;
    text-transform: uppercase;    
    background-color: #1f69a5;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#2e8ad1), to(#1f69a5));
    background-image: -webkit-linear-gradient(top, #2e8ad1, #1f69a5);
    background-image: -moz-linear-gradient(top, #2e8ad1, #1f69a5);
    background-image: -ms-linear-gradient(top, #2e8ad1, #1f69a5);
    background-image: -o-linear-gradient(top, #2e8ad1, #1f69a5);
    background-image: linear-gradient(top, #2e8ad1, #1f69a5);
    -moz-border-radius: 3px;
    -webkit-border-radius: 3px;
    border-radius: 3px;      
    text-shadow: 0 1px 0 rgba(0, 0 ,0, .3);
    -moz-box-shadow: 0 1px 0 rgba(255, 255, 255, 0.3) inset, 0 1px 0 #fff;
    -webkit-box-shadow: 0 1px 0 rgba(255, 255, 255, 0.3) inset, 0 1px 0 #fff;
    box-shadow: 0 1px 0 rgba(255, 255, 255, 0.3) inset, 0 1px 0 #fff;
}
 
.form-wrapper #submit:hover,
.form-wrapper #submit:focus {		
    background-color: #2e8ad1;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#1f69a5), to(#2e8ad1));
    background-image: -webkit-linear-gradient(top, #1f69a5, #2e8ad1);
    background-image: -moz-linear-gradient(top, #1f69a5, #2e8ad1);
    background-image: -ms-linear-gradient(top, #1f69a5, #2e8ad1);
    background-image: -o-linear-gradient(top, #1f69a5, #2e8ad1);
    background-image: linear-gradient(top, #1f69a5, #2e8ad1);
}	
 
.form-wrapper #submit:active {
    outline: 0;    
    -moz-box-shadow: 0 1px 4px rgba(0, 0, 0, 0.5) inset;
    -webkit-box-shadow: 0 1px 4px rgba(0, 0, 0, 0.5) inset;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.5) inset;    
}
 
.form-wrapper #submit::-moz-focus-inner {
    border: 0;
}

/*стиль текста*/
H1 { 
    font-family: Arial, Helvetica, Verdana, sans-serif; /* Гарнитура шрифта */ 
    font-size: 110%; /* Размер текста */ 
    font-weight: lighter; /* Светлое начертание */ 
   }
</style>
