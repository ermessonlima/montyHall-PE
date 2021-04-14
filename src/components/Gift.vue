<template>
  <div class="gift">
      <div class="gift-tie-1"></div>
      <div class="gift-tie-2">
          <p class="nota">10</p>
          <p class="nota2">Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups
              
          </p>
      </div>
  
      <div class="gift-body"></div>
  </div>
</template>

<script>

export default {
    name: 'Gift'
}
</script>

<style>
.gift {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    z-index: 10;
    margin-bottom: 80px;
}

.gift-body {
    width: 90px;
    height: 130px;
    background-color: #ffffff;
}
.gift-tie-1 {
    position: absolute;
    width: 15px;
    height: 85px;
   
}
.nota {
    font-size: 20px;
    color: red;
    margin-top: 10px;

}

.nota2 {
    font-size: 5px;
    color: black;
    margin-top: 10px;

}
.gift-tie-2 {
    justify-content: center;
    align-self: center;
    align-items: center;
    text-align: center;
    position: absolute;
    top:5px;
    width: 40px;
    height: 40px;
  border-radius: 20px;
   border: 2px solid red;
  
}
</style>