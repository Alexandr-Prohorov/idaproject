<template>
  <div class="sidebar">
    <div class="sidebar__title">Каталог</div>
    <ul class="sidebar__nav">
      <li class="sidebar__catalog__nav" v-for="item in items" :key="item.id">{{item.name}}</li>

    </ul>
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
     .get(`https://frontend-test.idalite.com/api/product-category`)
     .then((result) => {
       this.items = result.data
     });
  },

}
</script>



<style>
.sidebar{
  margin-top: 100px;
  display: inline-block;
  margin-left: 88px;
}

.sidebar__title{
  font-size: 32px;
  font-weight: 700;
}

.sidebar__nav{
  padding: 0;
  display: flex;
  flex-direction: column;

}

.sidebar__catalog__nav{
  list-style-type: none;
  margin-bottom: 16px;

}

.sidebar__catalog__nav:last-child{
  margin-bottom: 0;
}

.sidebar__catalog__nav:after{
    background-color: #333333;
    display:block;
    content:"";
    height: 2px;
    width: 0%;
    transition: width .3s ease-in-out;
}

.sidebar__catalog__nav:hover:after,
.sidebar__catalog__nav:focus:after {
    width: 100%;
}

</style>
