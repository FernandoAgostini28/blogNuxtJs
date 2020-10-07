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

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
