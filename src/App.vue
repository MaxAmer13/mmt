<template>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.CenterBox{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
}

.LineCenterBox{
    display: flex;
    justify-content: center;
    height: 100vh;
}

.form-container {
    width: 350px;
    height: 370px;
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    border-radius: 10px;
    box-sizing: border-box;
    padding: 20px 30px;
  }

  .Box{
    width: 350px;
    height: 550px;
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    border-radius: 10px;
    box-sizing: border-box;
    padding: 20px 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .Tournament{
    width: 350px;
    height: 200px;
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    border-radius: 10px;
    box-sizing: border-box;
    padding: 20px 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top:20px;
  }

  .form-container-inscri {
    width: 350px;
    height: 420px;
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    border-radius: 10px;
    box-sizing: border-box;
    padding: 20px 30px;
  }

  .title {
    text-align: center;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    margin: 10px 0 30px 0;
    font-size: 28px;
    font-weight: 800;
  }

  .subtitle{
    text-align: center;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    margin: 0px 0 10px 0;
    font-size: 20px;
    font-weight: 800;
  }

  .form {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 18px;
    margin-bottom: 15px;
  }

  .input {
    border-radius: 20px;
    border: 1px solid #c0c0c0;
    outline: 0 !important;
    box-sizing: border-box;
    padding: 12px 15px;
  }

  .page-link {
    text-decoration: underline;
    margin: 0;
    text-align: end;
    color: #747474;
    text-decoration-color: #747474;
  }

  .page-link-label {
    cursor: pointer;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    font-size: 9px;
    font-weight: 700;
  }

  .page-link-label:hover {
    color: #000;
  }

  .form-btn {
    padding: 10px 15px;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    border-radius: 20px;
    border: 0 !important;
    outline: 0 !important;
    background: teal;
    color: white;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }

  .form-btn-green {
    padding: 10px 15px;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    border-radius: 20px;
    border: 0 !important;
    outline: 0 !important;
    background: green;
    color: white;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }

  .form-btn-red {
    padding: 10px 15px;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    border-radius: 20px;
    border: 0 !important;
    outline: 0 !important;
    background: red;
    color: white;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }

  .btn{
    padding: 10px 15px;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    border: 0 !important;
    outline: 0 !important;
    background: teal;
    color: white;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }

  .form-btn:active {
    box-shadow: none;
  }

  .sign-up-label {
    margin: 0;
    font-size: 10px;
    color: #747474;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  }

  .sign-up-link {
    margin-left: 1px;
    font-size: 11px;
    text-decoration: underline;
    text-decoration-color: teal;
    color: teal;
    cursor: pointer;
    font-weight: 800;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
          "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  }

  .buttons-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    margin-top: 20px;
    gap: 15px;
  }

#noms{
    display: flex;
    flex-direction: row;
    justify-content: center;
}

#noms input{
    width: 140px;
}

#noms input:first-child{
    margin-right: 8px;
}

.nav-links{
  display: flex;
  align-items: center;
  background: #fff;
  padding: 20px 15px;
  border-radius: 12px;
  box-shadow: 0 5px 10px rgba(0,0,0,0.2);
}

.nav-links li{
  list-style: none;
  margin: 0 12px;
}
.nav-links li a{
  position: relative;
  color: #333;
  font-size: 20px;
  font-weight: 500;
  padding: 6px 0;
  text-decoration: none;
}
.nav-links li a:before{
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3px;
  width: 0%;
  background: teal;
  border-radius: 12px;
  transition: all 0.4s ease;
}
.nav-links li a:hover:before{
  width: 100%;
}
.nav-links li.upward a:before{
  width: 100%;
  bottom: -5px;
  opacity: 0;
}
.nav-links li.upward a:hover:before{
  bottom: 0px;
  opacity: 1;
}

nav{
    width:100%;
    display: flex;
    justify-content: center;
}

.select{
    border: 1px solid #c0c0c0;
    outline: 0 !important;
    box-sizing: border-box;
    padding: 12px 15px;
}

.profile{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: 0px 50px 0px 50px;
}

.profile h2{
    margin: 0px 50px 0px 70px;
}

#Commentary{
  display: flex;
  flex-direction: column;
  gap:30px;
  width:800px;
}

#Commentary div {
  display: flex;
  flex-direction: row;
  gap:5px;
  justify-content: space-between;
}

#commentary div input{
  width: 300px;
}

#commentary textarea{
  height:400px;
  width: 800px;
}

#apage{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.select{
    width: 350px;
    height: 340px;
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    border-radius: 10px;
    box-sizing: border-box;
    padding: 20px 30px;
    list-style-type: none;
}

.select li{
  border-top: 3px solid black;
  border-bottom: 3px solid black;
  border-radius: 10px;
  margin: 5px 0px 5px 0px;
  padding: 10px;
}
</style>
