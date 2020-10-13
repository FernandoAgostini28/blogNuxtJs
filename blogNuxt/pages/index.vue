<template>

 <!-- classe principal-->
  <div class="container">
    <!-- cabeçalho -->
    <div class="header">
      <h1>Melhor Blog de Programação</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut maxime facilis tempora neque tempore necessitatibus nesciunt, fuga excepturi quam eveniet aliquam hic error accusantium quis officia ad temporibus velit doloribus.</p>
      <!-- Formulario -->
      <div class="form">
        <h1>Novo Artigo</h1>
        <form @submit.prevent="addArtigo">
          <label label class= "labelForm" for="nome">
            Titulo:
          </label>
          <input class="textForm" v-model="newTitulo" type="text" placeholder="Novo titulo" name=" newTitulo" id="newTitulo" value=""/>
          <label label class="labelForm" for="mensagem">
            Mensagem:
          </label>
          <textarea class="textForm" v-model="newArtigo" type="text" placeholder="Nova Mensagem" name=" newArtigo" id="newArtigo" value=""> </textarea>
          <input class="buttonGreen" type="submit" value="Enviar Artigo"/>
        </form>
      </div>
    </div>
    <!-- cards dos artigos -->
    <div class="content">
      <h1>
          Artigos
      </h1>
      <ul> 
        <!-- percorrendo o array com os artigos-->
          <li  class="liCard" v-for=" (art , index) in artigos" :key="index"> 
            <div class="card">
              <span class="card-header"><h2 class="tituloArt" @click="exibirArtigo(index)">{{art.titulo}}</h2>
              </span> 
              <!-- Exibe o texto do artigo selecionado-->
              <div  v-if="artigoAberto === index" id="artigo">{{art.artigo}}</div>
              <!-- botao para remover artigo -->
              <button class="btn" @click="removeArt(art)" type="button">remove</button>
            </div>
          </li>
        </ul>
    </div>
    <!-- rodapé -->
    <div class="footer">
      <span> Todos os direitos reservados</span>
    </div>    
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: '',
        newTitulo: '',
        newArtigo:'',
        artigoAberto: null,
        artigos: []
     
    };
  },

   /*metodo adiciona novo artigo ao Array*/
    methods:{
        addArtigo() {
            this.artigos.push({
                titulo: this.newTitulo,
                artigo: this.newArtigo,
                show: false,
                
            });
            this.newTitulo = '';
            this.newArtigo = '';
        },
        /* metodo para comparar  abrir artigo*/
        exibirArtigo(index){
          this.artigoAberto = index;
        },
        
          
            
        
        /* metodo para remover artigo*/
        removeArt(art) {
            const todoIndex = this.artigos.indexOf(art);
            this.artigos.splice(todoIndex, 1);
        }
           
        
    }
}
</script>

<style>
   
  
</style>
