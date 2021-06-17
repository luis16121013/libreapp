<script>
  export let position=10
  export let duration=0.6
</script>

<i 
   style={`
             left:${position}px;
             animation-duration:${duration}s;
    `}>

</i>

<style>
   i {
    position:absolute;
    top:0;
    width:1px;
    height:100px;
    background:#fff;
    animation: animateStar linear infinite;
    animation-duration:1s;
  }
  @keyframes animateStar {
    0%{
      transform: translateY(0);
    }
    100%{
      transform: translateY(100vh);
    }
  }
</style>
