<template>
  <div id="app">
    <ul id="footer">
      <li>
        <i class="iconfont icon-weibiaoti1 btn"></i>
      </li>
      <li class="cartli">
        <i class="iconfont icon-gouwuche cart"></i>
        <span class="goodsNumber">0</span>
      </li>
      <li>
        <i class="iconfont icon-wode1 btn"></i>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'IndexFooter',
}
</script>

<style>
  /*#app{
    width:3.75rem;
    position:fixed;
    bottom:0;
  }*/
  #footer{
    width:3.75rem;
    background:#E6E6E9;
    color:#333;
    position:fixed;
    bottom:0;
    padding:0 15%;
    height:.59rem;
    display:flex;
    justify-content:space-between;
    align-items:center;
  }
  #footer>li>i{
    font-size:.3rem;
  }
  .icon-weibiaoti1{
    color:#A2A59F;
  }
  .cartli{
    width:.52rem;
    height:.52rem;
    position:relative;
  }
  #footer>li>.cart{
    display:block;
    width:.52rem;
    height:.52rem;
    border-radius:50%;
    background:#F4403F;
    color:#fff;
    font-size:.4rem;
    line-height:.52rem;
    text-align:center;
    position:absolute;
    bottom:.1rem;
  }
  .goodsNumber{
    display:block;
    width:.2rem;
    height:.2rem;
    border-radius:50%;
    border:0.01rem solid #fff;
    position:absolute;
    right:0;
    top:-0.15rem;
    background:#F4403F;
    text-align:center;
    line-height:.2rem;
    color:#fff;
  }
</style>