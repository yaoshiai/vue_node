<template>
    <div>
        这里是购物车组件
      <span>{{$route.query.goodsId}}</span>
      <span>{{$route.params.cartId}}</span>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                msg: `hello vue`
            }
        },

    }
</script>


