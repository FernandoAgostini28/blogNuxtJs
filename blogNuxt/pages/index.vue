<template>
  <div class="container">
    
    <div class="content">
      <h1 h1 class="titleForm">
        Novo Artigo
      </h1>
      <form name="contato" action=" " method="post">
        <label label class= "labelForm" for="nome">
          Titulo:
        </label>
        <input class="textForm" name="name" id="name"/>
        <label label class="labelForm" for="mensagem">
          Mensagem:
        </label>
        <textarea class="textForm" name="message"  id="message"> </textarea>
        <input class="buttonGreen" type="submit" value="Send message"/>
      </form>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
 
  

</style>
