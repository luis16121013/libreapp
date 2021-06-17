<script>
  import {link} from 'svelte-routing'
  export let title="tittlecard"
  export let textButton="Comenzar"
  export let url="/ingresar"
</script>

<div class="col-12 col-sm-6 col-md-4 col-lg-3 col-xl-2" >
  <div class="card efect" style="width: 100%;">
    <div class="card-body">
      <h5 class="card-title">{title}</h5>
      <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
      <div class="content-btn">
        <a 
           href={url} 
           class="btn btn-outline-primary"
           use:link
        >
          {textButton}
        </a>
      </div>
    </div>
  </div>
</div >

<style>
  .efect{
		margin:10px auto;
    box-shadow:0 10px 10px 10px rgba(0,0,0,0.1);
	}
  .efect:hover{
    background-color:rgba(145,145,145,0.1);
  }
  .content-btn {
    display:flex;
    justify-content:flex-end;
  }
</style>
