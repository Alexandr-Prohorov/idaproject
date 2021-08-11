<template>
  <div class="container">
    <Header/>
    <div class="container__content">
      <Sidebar/>
      <div class="catalog__cart">
        <Cart/>
        <Cart/>
        <Cart/>
        <Cart/>
        <Cart/>
        <Cart/>
        <Cart/>

      </div>
    </div>
  </div>
</template>

<script>
export default {}
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
