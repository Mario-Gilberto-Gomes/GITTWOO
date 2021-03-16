<template>

    <div id="mymodal" class="modal is-hidden is-visuallyHidden">
        <div class="modal-content">
            <span id="closemodal" class="close">&times;</span>
            <p> Teste modal</p>
          </div>
    </div>      
    <button id="mybtn">Open Modal</button>



</template>


<script>
// Get Modal 
var modal= document.getElementById('myModal');
//Get the main conteiner and body
var body = document.getElementsByTagName('body');
var container = document.getElementById('myConteiner');
//Get the open button 
var btnOpen =document.getElementById("myBtn");
//Get the close button
var btnClose = document.getElementById("closeModal");
// open the modal
btnOpen.onclick = function ()
{
     modal.className="Modal is-visuallyHiden";
     setTimeout (function(){
     container.className = "MainContainer is blurred";
     modal.className = "Modal";
     }, 100 );
     container.parentElement.className= "ModalOpen";

}
//close de modal
btnClose.onclick = function(){

      modal.className="Modal is-visuallyHiden";
      body.className="";
      container.className = "MainContainer is blurred";
      modal.className = "Modal";
      container.parentElement.className= "";
}
//when users clicks anywhere outside of the modal, close it.
window.onclick= function (event){
    if (event.target==modal)
    {
        modal.className = "Modal is-Hidden";
        body.className="";
        container.className="Maincontainer";
        container.parentElement.className="";

    }
} 




</script>




<style lang="css" scoped>

.Modal{
display: block;
position: fixed;
left: 0;
right: 0;
top:  0;
z-index: 9999;
width: 100%;
height: 100%;
padding-top: 100px;
background-color: #0000;
background-color: rgba (0, 0 , 0 , 0.4);
-webkit-transition: 0.5s;
overflow: auto;
transition: all 0.3s linear;

}   

.Modal-content{
    background-color: #fefefefe;
    margin: auto;
    padding: 20px;
    border-radius: 4px;
    max-width: 300px;
    height: 450px;
}

.ModalOpen{

    overflow: hidden;

}
.is-hidden{
    display: hidden;

}
.is-visuallyHidden {
    opacity: 0;
}
.Close{
    color:#aaaaaa;
    float: right;
    font-size: 16px;

}
.close:hover, .close:focus{
    color: #0000;
    text-decoration: none;
    cursor: pointer;
}
.is-blurred{
    filter: blur(2px);
    -webkit-filter: blur(2px);
}

</style>