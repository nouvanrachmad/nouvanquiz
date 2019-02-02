<template>
  <div class="hello">
    <h1 v-if="show">{{ msg }}</h1>
    <h1 v-else>Judul Disembunyikan</h1>
    <p>Skor : {{skor}}/3</p>
    <p>{{ nama}}</p>
    <input type="text" v-model="nama">
    <button type="button" v-on:click="hideTitle">Click Me</button>
    <br>
    <!--SOAL1-->
    <li v-for="s in soal">
    <h3>{{s}}</h3>
    <jawaban1 v-for="j in jawaban1">
    <br>
    <input type="radio" v-on:click="increment" value="A. Dont look back in anger">
    {{j}}
    </jawaban1>
    <br>
    <jawaban2 v-for="a in jawaban2">
    <input type="radio" v-on:click="increment" value="B. Perfect">
    {{a}}
    </jawaban2>
    <br>
    <jawaban3 v-for="w in jawaban3">
    <input type="radio" v-on:click="increment" value="C. SAD!">
    {{w}}
    </jawaban3>
    <br>
    <jawaban4 v-for="b in jawaban4">
    <input type="radio" v-on:click="increment" value="D. Cinta di pantai bali">
    {{b}}
    </jawaban4>
    <!--SOAL2-->
      <li v-for="o in soal2">
    <h3>{{o}}</h3>
    <option1 v-for="p in option1">
    <br>
    <input type="radio" v-on:click="increment" value="A. China">
    {{p}}
    </option1>
    <br>
    <option2 v-for="t in option2">
    <input type="radio" v-on:click="increment" value="B. Russia">
    {{t}}
    </option2>
    <br>
    <option3 v-for="i in option3">
    <input type="radio" v-on:click="increment" value="C. Phillipina">
    {{i}}
    </option3>
    <br>
    <option4 v-for="n in option4">
    <input type="radio" v-on:click="increment" value="D. Brazil">
    {{n}}
    </option4>
     <!--SOAL3-->
      <li v-for="l in soal3">
    <h3>{{l}}</h3>
    <choose1 v-for="c in choose1">
    <br>
    <input type="radio" v-on:click="increment" value="A. Ronaldo">
    {{c}}
    </choose1>
    <br>
    <choose2 v-for="e in choose2">
    <input type="radio" v-on:click="increment" value="B. Messi">
    {{e}}
    </choose2>
    <br>
    <choose3 v-for="s in choose3">
    <input type="radio" v-on:click="increment" value="C. Fabregas">
    {{s}}
    </choose3>
    <br>
    <choose4 v-for="h in choose4">
    <input type="radio" v-on:click="increment" value="D. Ronaldowati">
    {{h}}
    </choose4>
    </li>
  </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data : function() {
  return{
    nama: 'Nouvan',
    show: true,
    skor: 0,
    soal : ['1. Lagu apa yang dinyanyikan oleh ed sheeran ?'],
    jawaban1 : ['A. Dont look back in anger'],
    jawaban2 : ['B. Perfect'],
    jawaban3 : ['C. SAD!'],
    jawaban4 : ['D. Cinta di pantai bali'],
    soal2 : ['2. Negara paling padat penduduknya ?'],
    option1 : ['A. China'],
    option2 : ['B. Russia'],
    option3 : ['C. Phillipina'],
    option4 : ['D. Brazil'],
    soal3 : ['3. Siapa pemain terkenal di real madrid?'],
    choose1 : ['A. Ronaldo'],
    choose2 : ['B. Messi'],
    choose3 : ['C. Fabregas'],
    choose4 : ['D. Ronaldowati']
    }
    },
  methods: {
    hideTitle() {
      this.show = !this.show
    },
    increment() {
    var value = event.target.value;
    if (value === "B. Perfect"){
    this.skor++;
    }else if (value === "A. China"){
    this.skor++;
    }else if (value === "A. Ronaldo"){
    this.skor++;
    }else{
			this.skor--;
		}
    }
  },
  mounted: function () {
    this.nama = 'Nouvan Rachmad'
  }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
