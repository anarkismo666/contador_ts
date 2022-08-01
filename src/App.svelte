<script lang="ts">
    let counter:number = 0;
 
	const modifyCiounter=(value:number):number => counter = counter + value;

	/*
	// Asi estaba
    const add=() : void =>{
        counter++;
    }

    const less=() : void =>{
        counter--;
    }

   
	*/
	const reset=() : void =>{
      counter=0;
    }
</script>

<main>
  
  <div>
	<h1>Contador App {new Date()} </h1>
	<hr>
	<h2 class={counter<0? "negativo":"positivo"}>Counter {counter}</h2>
	<button class="add" on:click={()=>modifyCiounter(1)}>+1</button>
	<button class="less" on:click={()=>modifyCiounter(-1)}>-1</button>
	<button class="reset" on:click={reset}>Reset</button>
  </div>
  
</main>

<style>

  div{
	text-align: center;
  }
  button{
    font-size: 2rem;
    margin: 0 0.4 rem;
    border-radius: 5px;
  }

  button:hover{
    cursor: pointer;
  }

  .add{
    background-color: #26b231;
  }

  .add:active{
    background-color: #155c1b;
    
  }

  .less{
    background-color: #3a9aea;
  }
  .less:active{
    background-color: #26679c;
    
  }

  .reset{
    background-color: tomato;
  }
  .reset:active{
    background-color: rgb(166, 74, 58);
    
  }

  .negativo{
      color:red
  }

  .positivo{
      color:blue
  }
</style>
