<template>
  <div class="contaiiner">
    <form action="" method="">
       <h1 class="h1">Cadastro para Tech Talent Moz</h1>
          <div>
          <label 
           class="label" 
           for="nome"> 
            Nome e Apelido 
          </label>
         </div>
         <div>
           <input 
            class="input" 
             type="text" 
              placeholder="Ex: Jhon Doe" required />
           </div>
            <div>
            <label 
           class="label" 
            for="email"> 
            E-mail
           </label>
           </div>
           <div>
           <input
           class="input"
           type="email"
           placeholder="Ex:jhon@email.com"
           required
           autocomplete="on"
           />
           </div>
           <div>
           <label class="label" for="Skills"> Skills </label>
           </div>
           <div>
           <input
           class="input"
           type="text"
           placeholder="Ex: UX Designer, PHP, HTML, CSS, etc..."
           />
           </div>
           <div>
            <label class="label" for="taxa"> Taxa por Hora</label>
           </div>
           <div>
           <input
           class="input"
           type="number" min="0"
           placeholder="Ex: 250 por hora"
           require/>
           </div>
           <div>
           <label 
           class="label" 
           for="disponibilidade" > 
            Disponibilidade
           </label>
           </div>
           <div>
           <select id="disponibilidade">
           <option value="Disponibilidade" readonly> Disponibilidade</option>
           <option value="Full Time" > Full time</option>
           <option value="Part-Time"> Part Time</option>
          
            </select>
            </div>
 
             <div>
             <label class="label" for="Portifolio"> Link do Portifolio</label>
             </div>
             <div>
             <input 
             class="input" 
             type="url" 
             placeholder="Link do Portifolio"
             />
              </div>
                <div>
              <label 
              class="label" 
             for="Linkdin"> 
            Link do Linkedin
             </label>
             </div>
             <div>
             <input 
             class="input" 
             type="url" 
             placeholder="Link do linkedin" />
             </div>
 
             <div>
             <label 
             class="label" 
             for="Github">Link do Github
             </label>
             </div>
             <div>
             <input 
              class="input" 
             type="url" 
             placeholder="Link do Github" />
             </div>
             <!-- input para carregar foto-->
             <div class="inputfile-box">
          <input 
           type="file" 
           id="file" 
           class="inputfile" 
           @change="uploadFile" required/>

           <label id="alabel" for="file" placeholder="Adicionar Foto" > Adicionar Foto
            <div id="anexar">
              <span id="file-name" class="file-box"> {{inputFileText}}</span>
            <span class="file-button">
              <i class="fa fa-upload" aria-hidden="true"></i>
                Anexar
                 </span>
            </div>
             </label>
          </div>



     

      <div>
        <button class="btn" input type="Submit">Registar</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {

  data(){
    return{
      inputFileText: "",
    }
  },
  methods: {
    uploadFile: function(e) {
      console.log(e.target.value);
      this.inputFileText = e.target.value;
    }
  }
}
</script>





<style lang="css" scoped>
.contaiiner {
  width: 821px;
  height: 1433px;
  background: #f7f8fa;
  box-shadow: 0px 2px 20px 9px rgba (31, 31, 31, 0, 04);
  border-radius: 38px;
  margin-left: 500px;
  margin-top:186px ;
  margin-right: 500px;
}

.input {
  width: 666px;
  height: 56px;
  margin-top: 16px;
  background: #ffffff;
  border: 1px solid rgba(207, 216, 220, 0.5);
  border-radius: 6px;
  margin-left: 68px;
  margin-bottom: 44px;
  padding-left: 12px;
  text-align: left;
  font-family: Roboto;
  font-style: normal;
  font-size: 16px;
  line-height: 14px;
  color: #78909c;
  display: flex;
}

.h1 {
  font-family: circular std;
  font-style: normal;
  font-weight: bold;
  font-size: 48px;
  margin-left: 58px;
  margin-right: 30px;
  margin-top: 33px;
  margin-bottom: 33px;
  display: flex;
  justify-content: center;
  align-content: center
  
}

.btn {
  width: 666px;
  height: 56px;
  background: linear-gradient(135deg, #79beff 0%, #448aff 100%);
  border-radius: 6px;
  margin-right: 39px;
  margin-top: 40px;
  margin-left: 68px;
  margin-bottom: 157px;
  border: none;
}

.label{
  margin-left: 68px;
  margin-top: 33px;
  font-family: Roboto;
  font-weight: normal;
  font-size: 16px;
  line-height: 13px;
  
}
#disponibilidade {
  width: 680px;
  height: 56px;
  margin-top: 16px;
  background: #ffffff;
  border: 1px solid rgba(207, 216, 220, 0.5);
  border-radius: 6px;
  margin-left: 68px;
  margin-bottom: 56px;
  padding-left: 12px;
  padding-right: 20px;
  text-align: left;
  font-family: Roboto;
  font-style: normal;
  font-size: 16px;
  line-height: 14px;
  color: #78909c;
  display: flex;
}
.inputfile-box {
  position: relative;
}

.inputfile {
  display: none;
  

}

.container {
  display: flex;
  width: 666px;
}

.file-box {
    width: 563px;
    height: 61px;
    border: 1px solid rgba(207, 216, 220, 0.5);
    background: #ffffff;

    border-radius: 6px;
 
}

.file-button {
    width: 104px;
    height: 61px;
    background: linear-gradient(135deg, #79beff 0%, #448aff 100%);
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
    
}

#anexar{
  display: flex;
  border-radius: 6px;
  margin-left: 68px;
}

#alabel{

  margin-left: 68px;
  margin-top: 33px;
  margin-bottom: 23px;
  font-family: Roboto;
  font-weight: normal;
  font-size: 16px;
  line-height: 13px;
}


</style>

