<template>
  <div class="container">
    <Header/>
    <div class="container__content">
      <Sidebar/>
      <div class="catalog__cart">
        <Cart v-for="item in items" :key="item.id" :item="item"/>
      </div>
    </div>
    <Bascet/>
  </div>
</template>

<script>
export default {

  data: function(){
    return{
      items:[]
    };
  },

  methods: {},
  mounted(){
    this.$axios
     .get(`https://frontend-test.idalite.com/api/product`)
     .then((result) => {
       this.items = result.data
     });
  },

}
</script>


<style>

body{
  @import url('https://fonts.googleapis.com/css2?family=PT+Sans:wght@400;700&display=swap');
  font-family: 'PT Sans', sans-serif;
  margin: 0;
  font-size: 16px;
}

.container{
  width: 100%;
  margin: 0 auto;
}

.container__content{
  display: flex;
}


.catalog__cart{
  display: flex;
  flex-wrap: wrap;
  width: 90%;

  margin-top: 152px;
  margin-left: 42px;

}

</style>
