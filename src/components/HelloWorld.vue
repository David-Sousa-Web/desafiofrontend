<template>
  <form class="form-content">
    <div class="header">
      <div class="content">
        <p>Formulário<br/>para compra de</p>
        <h3>Pacote de adesivos</h3>
      </div>
      <div class="icon fa-7x">
        <i class="fa-solid fa-box-open"></i>
      </div>
    </div>
    <div class="options">
      <h4>Quais Adesivos:</h4>
      <div class="options-container">
        <input type="checkbox" id="react" name="bibliotecas" value="reactlang">
        <label for="react" class="label">React</label>
      </div>
      <div class="options-container">
        <input type="checkbox" id="vue" name="bibliotecas" value="vuelang">
        <label for="vue" class="label">Vue</label>
      </div>
      <div class="options-container">
        <input type="checkbox" id="angular" name="bibliotecas" value="angularlang">
        <label for="angular" class="label">Angular</label>
      </div>
    </div>
    <div class="quantidade">
      <h4>Quantos adesivos de cada?</h4>
      <div class="contador">
        <div class="contador-container">
         <button id="menos" class="menos" v-on:click="CLickM()" type="button">-</button>
          <p type="text" value="0"  class="valor" maxlength="7" onkeypress="return event.charCode >= 48 && event.charCode <= 57">{{ count }}</p>         
         <button class="mais" v-on:click="ClickP()" type="button">+</button> 
        </div>
      </div>
    </div>
    <div class="observacao">
      <h4>Observeções:</h4>
      <div class="message">
        <textarea placeholder="alguma dúvida? recado?" maxlength="200" ></textarea>
      </div>
    </div>
    <div class="botao-content">
        <button @click="submit">Enviar</button>
    </div>
  </form>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data(){
      return{
        count: 0,
      };
    },
    methods:{
      ClickP(){
       this.count++;
      },
      CLickM(){
        this.count--;    
      },
      submit(){
        alert("enviado com sucesso")
      }
      
    },
    
}

</script>

<!--   -->
<style scoped>
.form-content{
  background-color: white;
  width: 430px;
  height: 650px;
  margin-right: 50%;
  margin-left: 35%;
  border-radius: 8px; 
  -webkit-box-shadow: 3px 3px 13px 0 #000000;
  -moz-box-shadow: 3px 3px 13px 0 #000000;
  box-shadow: 3px 3px 13px 0 #000000;
}
.header{
  background-color: #2e3675;
  width: 100%;
  height: 150px;
  border-radius: 8px 8px 50% 50% / 8px 8px 65% 30%;
  padding-left: 30px;
  padding-top: 20px;
  display: flex;
}

.header p{
  color: rgba(255, 255, 255, .7);
  font-size: 18px;
  font-weight: 100;
}

.header h3{
  color: white;
  font-weight: 500;
}
.icon{
  margin-left: 50px;
  margin-right: 40px;
}
.fa-solid{
  color: rgb(31, 37, 78);
}
.options{
  padding: 25px;
}
.options-container{
  margin-top: 10px;
}
.label{
  padding-left: 3px;
}
.quantidade{
  padding-left: 20px;
}
.contador-container{
  margin-top: 10px;
  display: flex;
}
.valor{
  width: 60px;
  margin-left: 5px;
  margin-right: 5px;
  background-color: rgb(177, 182, 214);
  border: 1px solid #2e3675;
  border-radius: 5px;
  padding: 3px;
}
.menos{
  width: 30px;
  height: 30px;
  font-size: large;
  background: #2e3675;
  border: none;
  border-radius: 4px;
  color: white;
}
.mais{
  font-size: large;
  width: 30px;
  height: 30px;
  background: #2e3675;
  border: none;
  border-radius: 4px;
  color: white;
}
.observacao{
  padding: 20px;
}
.message{
  margin-top: 10px;
}

textarea{
  width: 385px;
  height: 100px;
  border: 1px solid #2e3675;
  border-radius: 8px;
  padding: 10px;
  background-color: rgb(177, 182, 214);
  resize: none;
}
.botao-content{
  background-color: rgb(177, 182, 214);
  width: 430px;
  height: 80px;
  margin-top: 32px;
  border-radius: 0px 0px 8px 8px;
  display: flex;
  padding: 20px;
  justify-content: flex-end;
}

button{
  width: 100px;
  height: 40px;
  background: #2e3675;
  border: none;
  border-radius: 4px;
  color: white;
}

</style>
