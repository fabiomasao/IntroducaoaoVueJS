<template>

	 <div class="slider">
      <h3>{{titulo}}</h3>
      <span v-on:mouseover="scrollEsquerda()" v-on:mouseout="clearScroll()" class="handle handlePrev active">
           <i class="fa fa-caret-left" aria-hidden="true"></i>
      </span>


      <div ref="scroller" class="row">
      <div class="row__inner">

         
      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>

      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>

      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>

      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>

      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>

      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>

      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>

      <Filme titulo="Assassin’s Creed" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></Filme>


       </div>
       </div> 


      <span v-on:mouseover="scrollDireita()" v-on:mouseout="clearScroll()"  class="handle handleNext active">
    <i class="fa fa-caret-right" aria-hidden="true"></i>
  </span>

    </div>
	


</template>

<script>

import Filme from './Filme.vue';
export default {
	name:'teste',
	props:['titulo'],
	components:{
		Filme
	},

	methods:{

      scrollDireita(){
      	const self = this;
        this.intervalo = setInterval(function(){ self.$refs.scroller.scrollLeft += 1 }  , 5);

      },

      scrollEsquerda(){
      	const self = this;
        this.intervalo = setInterval(function(){ self.$refs.scroller.scrollLeft -= 1 }  , 5);

      },

      clearScroll(){
      	const self = this;
        clearInterval(this.intervalo);


      }
    }

}
	

</script>


<style>



</style>