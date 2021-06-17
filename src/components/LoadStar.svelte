<script>
  import Stars from './Stars.svelte'
</script>

<div class="scene">
  <Stars message={"En desarrollo..."}/>
  <div class="rocket">
    <img src="https://github.com/libreapp/blob/master/public/rocket.png?raw=true" alt="rocket">
  </div>
</div>

<style>
  .scene{
    position:relative;
    width:100%;
    height:91vh;
    background-color:#01070a;
    overflow:hidden;
    display:flex;
    justify-content:center;
    align-items:center;
  }
  .rocket {
    position:relative;
    animation:animate 0.2s ease infinite;
  }
  @keyframes animate {
    0%,100%{
      transform: translateY(-2px);
    }
    50%{
      transform: translateY(2px);
    }
  }
  .rocket::before{
    content:'';
    position:absolute;
    bottom:-111px;
    left:44%;
    width:10px;
    height:110px;
    background:linear-gradient(#00d0ff,transparent);
  }
  .rocket::after{
    content:'';
    position:absolute;
    bottom:-111px;
    left:44%;
    width:10px;
    height:110px;
    background:linear-gradient(#00d0ff,transparent);
    filter:blur(20px);
  }
</style>
