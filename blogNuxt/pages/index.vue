<template >
  <div class = " container ">
    <h1 h1  class = " title ">
      Contato
    </h1>
    <div class = " content ">
      <form  name = " contato "  action = " "  method = " post ">
        <label label  class = " form-label "  for = " nome ">
          Titulo:
        </label >
        <input  class = " form-field "  name = " name "  id = " name " />
        <label label  class = " form-label "  for = " mensagem ">
          Mensagem:
        </label>
        <textarea  class = " form-field "  name = " message "  id = " message " > </textarea >
        <input  class = " form-button "  type = " submit "  value = " Send message "/>
      </form>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {

}

.content {
  box-sizing: border-box;
  width: 280px;
  padding: 8px ;
  border: 1px solid #ccc;
  box-shadow:0 2px 2px #aaa;
}

</style>
