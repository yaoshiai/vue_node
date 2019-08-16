<template>
  <div>
    <div>这是商品列表页面</div>
    <span>{{$route.params.goodsId}}</span>
    <span>{{$route.params.name}}</span>
    <router-link to="/goods/title">显示商品标题</router-link>
    <router-link to="/goods/image">显示商品图片</router-link>
    <div>
      <router-view></router-view>
    </div>
    <!--<router-link to="/cart">购物车</router-link>-->
    <router-link :to="{name:'cart',params:{cartId:123}}">购物车</router-link>
    <button @click="jump">button - 跳转到购物车页面</button>
  </div>
</template>

<script>
    export default {
        name: "goods-list",
        methods:{
          jump(){
            // this.$router.push('/cart');
            // this.$router.push({path:'/cart?goodsId=123'});
            this.$router.go(-2);
          },
        }
    }
</script>

<style scoped>

</style>
