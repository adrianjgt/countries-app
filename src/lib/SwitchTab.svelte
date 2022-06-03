<script>
const option1="Countries you want to visit";
const option2="Countries you have been";
let optionChange;
let optionState = [true, false]; 

function clicked(){
    if(optionState[0] == true){
        optionState = [false, true]
    } else{
        optionState = [true, false]
    };

    console.log("hello adrian", optionState);
};


</script>


<div on:click={clicked} class="box-grey" class:inactive = {optionState[0]==false}>
    <div class="box-green" class:move-block = {optionState[0]==false}/>
    <div class="options">
        <div class="option one" class:inactive = {optionState[0]==false}>{option1}</div>
        <div class="option two" class:inactive = {optionState[1]==false}>{option2}</div>
    </div>
</div>




<style>
    .box-grey{
        display:flex;
        align-items: center;
        height: 86px;
        width: 450px;
        background-color: #ccc;
        border-radius:20px;
        justify-content: flex-start;
        padding:0 10px;
        
    }


    .box-green{
        background-color: #00BBB6;
        width: 225px;
        height:70px;
        border-radius:15px;
        transition: all ease-in-out 500ms;
        
    }

    .options{
        position: absolute;
        height: 86px;
        width: 450px;
        display:flex;
        justify-content: space-between;
        align-items: center;
    }

    .option{
        color: white;
        font-family: 'Josefin Sans';
        text-align: center;
        width:225px;
    }

    .inactive{
        color:rgba(0, 0, 0, 0.2);
        transition: all ease-in-out 500ms;
    }
    
    .move-block{
        transform: translateX(100%);        
    }



   


</style>