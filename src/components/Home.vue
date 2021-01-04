<template>
  <v-app id="inspire" class="content">
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons"
      rel="stylesheet">
    <v-navigation-drawer
      v-model="drawer"
      app
      disable-resize-watcher="true"
    >
      <v-list dense>
        <v-list-item class="ml-6">
          <v-list-item-content class="ml-6">
            <v-img
                src="..\assets\logo-alpha.png"
                max-height="70"
                max-width="70"
                class="ml-6"
              ></v-img>
          </v-list-item-content>
          
        </v-list-item>
        <v-list-item link>
          <v-list-item-action>
            <i class="material-icons">keyboard_arrow_right</i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-action>
            <i class="material-icons">keyboard_arrow_right</i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Sobre</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-action>
            <i class="material-icons">keyboard_arrow_right</i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Vantagens</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-action>
            <i class="material-icons">keyboard_arrow_right</i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>REGISTRE-SE</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!-- BARRA SUPERIOR -->
    <v-app-bar
      app
      color="white"
      class="topbar"
      :height="navbarheight"
    >
      
      <v-app-bar-nav-icon class="d-flex d-md-none ml-3" color= "black" @click.stop="drawer = !drawer"><v-icon large color="black">mdi-menu</v-icon></v-app-bar-nav-icon>
      <v-container class="d-none d-md-flex" fluid>
        <v-row align-content="center">
          <v-col>
              <v-img
                src="..\assets\logo-alpha.png"
                max-height="70"
                max-width="70"
                class="d-none d-sm-flex ml-sm-6 ml-md-12"
              ></v-img>
            </v-col>
          <v-col xs="2" sm="8" md="6" lg="5" xl="4" class="mt-2" >
            <v-row>
              <!-- v-for="item in topmenu" :key="item" -->
              <v-col align="center"  >
                <a class="topitem" v-bind:class="{ selected: topmenu[0].selected }" href="#home">{{topmenu[0].item}}</a>
              </v-col>
              <v-divider 
                  class="py-3"
                  align="right"
                  :inset="inset"
                  vertical
                  inset
              ></v-divider>
              <v-col align="center"  >
                <a class="topitem" v-bind:class="{ selected: topmenu[1].selected }" :href="topmenu[1].link">{{topmenu[1].item}}</a>
              </v-col>
              <v-divider 
                  class="py-3"
                  align="right"
                  :inset="inset"
                  vertical
                  inset
              ></v-divider>
              <v-col align="center"  >
                  <a class="topitem" v-bind:class="{ selected: topmenu[2].selected }" :href="topmenu[2].link">{{topmenu[2].item}}</a>
              </v-col>  
            </v-row>
          </v-col>
          <v-col align="center" class="text-center pt-6 mt-2" >
            <a class="registrese" href="#">REGISTRE-SE</a>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>
    <!-- CONTEUDO CENTRAL -->
    <v-content>
      <v-container fluid pa-0 ma-0>
        <v-row  class="pa-0 ma-0 no-gutters">
          <v-col  class="pa-0 ma-0 no-gutters">
            <v-img id="home"
            src="../assets/bg1.jpg"
            lazy-src="..\assets\logo-alpha.png"
            class="grey lighten-2 div1"
            :height="homeheight"
            >
              <v-img id="home"
              src="../assets/alphaexperience.png"
              lazy-src="https://picsum.photos/id/11/100/60"
              class="alphaexp"
              :max-width="alphaexp"
              
              >
                <template v-slot:placeholder>
                  <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center"
                  >
                    <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                  </v-row>
                </template>
              </v-img>
              <template v-slot:placeholder>
                <v-row
                  class="fill-height ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-row>
              </template>
            </v-img>
            
          </v-col>
        </v-row>
        <v-row class="no-gutters">
          <v-col class="xs-12 ma-0 pa-0">
                <v-row  no-gutters  class="mt-n13 bimage div2" id="row2" >
                  <div class="row2 ma-0 pa-0">
                    <v-col class="ma-0 pa-0" no-gutters width="100vw">
                      <h1 :class="div1topstyle">O que é o Alpha Experience?</h1>
                      <h2 class="my-2 px-12  mx-md-12 bg2subt h2">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</h2>
                      <h1 style="margin-top:63px" class="bg2title h1">Como funciona?</h1>
                      <h2 :class="div1bottomstyle">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</h2>
                      <div class="triangleleft" style="color:white;"></div>
                      <div class="triangleright" ></div>
                    </v-col >

                  </div>

                </v-row>

          </v-col>


        </v-row>
        
        
        <v-row no-gutters>
          <v-col class="col-12 col-sm-12 text-center pt-8 vantagens h1"><vantagens>Vantagens</vantagens></v-col>
          <v-col class="col-12 col-sm-10 col-lg-10 col-xl-10 offset-sm-1 offset-sm-1">
            <div class="div3 pb-8">
                <v-row no-gutters>
                  <v-col class="col-12 col-sm-6 col-md-4 text-center">
                      <v-col class="text-center xs-12">
                        <i class="material-icons icon text-center">face</i>
                      </v-col>
                      <v-col class="py-2">
                        <vantagens class="titulo">Lorem ipsum dolor </vantagens>
                      </v-col>
                      <v-col class="pt-1 px-8 px-sm-2">
                        <vantagens class="subtitulo">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Obcaecati, nulla officia. I omnis quo animi, nihil quasi quam nulla!</vantagens>
                      </v-col>
                  </v-col>
                  <v-col class="col-12 col-sm-6 col-md-4 text-center">
                      <v-col class="text-center xs-12">
                        <i class="material-icons icon text-center">face</i>
                      </v-col>
                      <v-col class="py-2">
                        <vantagens class="titulo">Lorem ipsum dolor </vantagens>
                      </v-col>
                      <v-col class="pt-1 px-8 px-sm-2">
                        <vantagens class="subtitulo">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Obcaecati, nulla officia. I omnis quo animi, nihil quasi quam nulla!</vantagens>
                      </v-col>
                  </v-col>
                  <v-col class="col-12 col-sm-6 col-md-4 text-center">
                      <v-col class="text-center xs-12">
                        <i class="material-icons icon text-center">face</i>
                      </v-col>
                      <v-col class="py-2">
                        <vantagens class="titulo">Lorem ipsum dolor </vantagens>
                      </v-col>
                      <v-col class="pt-1 px-8 px-sm-2">
                        <vantagens class="subtitulo">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Obcaecati, nulla officia. I omnis quo animi, nihil quasi quam nulla!</vantagens>
                      </v-col>
                  </v-col>
                  <v-col class="col-12 col-sm-6 col-md-4 text-center">
                      <v-col class="text-center xs-12">
                        <i class="material-icons icon text-center">face</i>
                      </v-col>
                      <v-col class="py-2">
                        <vantagens class="titulo">Lorem ipsum dolor </vantagens>
                      </v-col>
                      <v-col class="pt-1 px-8 px-sm-2">
                        <vantagens class="subtitulo">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Obcaecati, nulla officia. I omnis quo animi, nihil quasi quam nulla!</vantagens>
                      </v-col>
                  </v-col>
                  <v-col class="col-12 col-sm-6 col-md-4 text-center">
                      <v-col class="text-center xs-12">
                        <i class="material-icons icon text-center">face</i>
                      </v-col>
                      <v-col class="py-2">
                        <vantagens class="titulo">Lorem ipsum dolor </vantagens>
                      </v-col>
                      <v-col class="pt-1 px-8 px-sm-2">
                        <vantagens class="subtitulo">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Obcaecati, nulla officia. I omnis quo animi, nihil quasi quam nulla!</vantagens>
                      </v-col>
                  </v-col>
                  <v-col class="col-12 col-sm-6 col-md-4 text-center">
                      <v-col class="text-center xs-12">
                        <i class="material-icons icon text-center">face</i>
                      </v-col>
                      <v-col class="py-2">
                        <vantagens class="titulo">Lorem ipsum dolor </vantagens>
                      </v-col>
                      <v-col class="pt-1 px-8 px-sm-2">
                        <vantagens class="subtitulo">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Obcaecati, nulla officia. I omnis quo animi, nihil quasi quam nulla!</vantagens>
                      </v-col>
                  </v-col>
                </v-row>
            </div>
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col class='col-xs-12 div4bg'>
            <div class="div4">
                <v-col class="xs-12 px-5 pt-8 text-center">
                  <h1 class="pt-8 pb-5 h1bg4 h1">
                    Ainda não nos conhece?
                  </h1>
                  <h2 class="pb-4 h2bg4 px-8 mx-lg-8 h2">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium dolores possimus alias quasi minima ipsum dolorem ad assumenda obcaecati facilis cupiditate temporibus!
                  </h2>
                </v-col>
                <v-col class="text-center pb-8">
                  <v-btn rounded color="white" class="txtbg4 mb-8">VER CARDÁPIO<i class="material-icons iconblack">keyboard_arrow_right</i></v-btn>
                </v-col>
            </div>
          </v-col>
        </v-row>
        <v-row class="div5" no-gutters>
            <v-col class="d-none d-md-flex py-8 pl-8 mt-2 justify-center" cols="12" md="4">
              <img src="../assets/mascote.webp" alt="" height="90%" align="center" style="" />
            </v-col>
            <v-col class="pb-8 my-5 ma-md-8 align-center" cols="12" md="7">
                <div class="contato mx-2 py-4 pr-2" ref="formcontato">
                  <v-row no-gutters>
                    <v-col class="pb-4" cols="12" md="12">
                      <h1 class="h1">Tem alguma dúvida?</h1>
                      <h3 class="h3">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.</h3>
                    </v-col>
                    <v-col class="d-flex pt-2 px-4 mt-0 pt-0" cols="12" md="6">
                      <v-row>
                        <v-col cols="12" class="py-0 my-0">
                          <h3 class="h3 text-left">SEU NOME</h3>
                        </v-col>
                        <v-col cols="12" class="pt-0 my-0">
                          <v-text-field outlined dense>
                            nome
                          </v-text-field>
                        </v-col>
                      </v-row>                 
                    </v-col>
                    <v-col class="d-flex pt-2 px-4 mt-0 pt-0" cols="12" md="6">
                      <v-row>
                        <v-col cols="12" class="py-0 my-0">
                          <h3 class="h3 text-left">E-MAIL</h3>
                        </v-col>
                        <v-col cols="12" class="pt-0 mt-0">
                          <v-text-field outlined dense>
                            email
                          </v-text-field>
                        </v-col>
                      </v-row>                 
                    </v-col>
                    <v-col class="d-flex pt-2 px-4 mt-0 pt-0" cols="12">
                      <v-row no-gutters>
                        <v-col cols="12">
                          <h3 class="h3 text-left">MENSAGEM</h3>
                        </v-col>
                        <v-col cols="12">
                          <v-textarea outlined dense>

                          </v-textarea>
                        </v-col>
                      </v-row>
                    </v-col> 
                  </v-row>  
                  
                </div>
            </v-col>
        </v-row>
      </v-container>
      
      </v-content>
      <!-- RODAPE -->
    <!-- <v-footer
        color="black"
        app
      >
        <span class="white--text">&copy; 2019</span>
    </v-footer> -->
  </v-app>
</template>

<script>
  export default {
    props: {
      source: String
    },
    computed: {
      homeheight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '250px'
          case 'sm': return '400px'
          case 'md': return '500px'
          case 'lg': return '550px'
          case 'xl': return '800px'
        }
      },
      navbarheight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '70px'
          case 'sm': return '100px'
          case 'md': return '110px'
          case 'lg': return '115px'
          case 'xl': return '115px'
        }
      },
      div1topstyle(){
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return 'mt-12 bg2title h1'
          case 'sm': return 'mt-12 pt-5 bg2title h1'
          case 'md': return 'mt-12 pt-5 bg2title h1'
          case 'lg': return 'mt-12 pt-5 bg2title h1'
          case 'xl': return 'mt-12 pt-12 bg2title h1'
        }
      },
      div1bottomstyle(){
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return ' pb-12 px-12 bg2subt h2'
          case 'sm': return ' pt-5 mx-2 px-12 bg2subt h2'
          case 'md': return ' pt-5 mx-12 px-12 bg2subt h2'
          case 'lg': return ' pt-5 mx-12 px-12 bg2subt h2'
          case 'xl': return ' pt-12 mx-12 px-12 bg2subt h2'
        }
      },
      alphaexp () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '45%'
          case 'sm': return '45%'
          case 'md': return '40%'
          case 'lg': return '35%'
          case 'xl': return '35%'
        }
      },
      bg2height(){
        switch(this.$vuetify.breakpoint.name){
          case 'xs': return '100%'
        }
        if (document.getElementById('row2') != null){
          var element = document.getElementById('row2');
          var height = element.clientHeight

          return height
        }
      }
    },
    data: () => ({
      drawer: false,
      topmenu:[
        {item:'Home',link:'#home',selected:true,separator:true},
        {item:'Sobre',link:'#sobre',selected:false,separator:true},
        {item:'Vantagens',link:'#vantagens',selected:false,separator:false}
      ],
      bg2height: '500px'
    }),
   
  }
</script>
<style scoped>
h1{
color:white;
font-family: Zilla Slab;
font-style: normal;
font-weight: 500;
font-size: 44px;
line-height: 56px;
/* or 127% */

text-align: center;
}
h2{
  font-family: Montserrat;
font-style: normal;
font-weight: 500;
color:white;
font-size:24px;
line-height: 158.47%;
/* or 30px */

text-align: center;
}
.topbar{
  height: 50px;
}
a{
  color:black !important;
  text-decoration:none;
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
}
.registrese{
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: 600;
  font-size: 22px;
  line-height: 26px;
}
a:hover{
  color:#C0A358 !important;
}
.selected{
 color:#C0A358 !important;
}
.content{
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: bold;
  font-size: 22px;
  line-height: 26px;
}
.alphaexp{
 top:25%;
 left:7%;
}
.material-icons{
  color:goldenrod;
}
.div1{
   height: 589px;
}
.div2{
  height:100%;
  left: 0px;
  top: 705px;
  background: rgba(57, 57, 55, 0.925); 
}
.bg2{
  background-image: "../assets/alphaexperience.png";
}
.row2{
  background: rgba(57, 57, 55, 0.8); 
}
.div3{
  background-color: white;
  /* height: 590px; */
}
.div4{
  
  background: linear-gradient(0.14deg, rgba(56, 56, 55, 0.75) -122.59%, rgba(192, 163, 88, 0.75) 92%);
}
.div5{
  width:100%;
  background: #FEAE39;
  padding:0px;
}
.div4bg{
  background-image: url('../assets/bg3.jpg');
  background-repeat:no-repeat;
  background-position: center;
  background-size:cover;
}
.bg2title{
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: 500;
  font-size: 44px;
  line-height: 56px;
  /* or 127% */

  text-align: center;

  color: #FFFFFF;

}
.bg2subt{
  font-family: Montserrat;
  font-style: normal;
  font-weight: 500;
  font-size: 19px;
  line-height: 158.47%;
  /* or 30px */

  text-align: center;

  color: #FFFFFF;

  opacity: 0.8;
}
.iconblack{
  color: #3C444C;
}
.triangleleft{
  /* position:absolute; */
  left:0px;
  width: 0; 
  height: 0; 
  transform: translate(0px, 4.11vw);
  border-left: 0px solid transparent;
  border-right: 50vw solid transparent;
  
  border-bottom: 4vw solid white;
}
.txtbg4{
  font-family: Montserrat;
  font-style: bold;
  font-weight: 1000;
  font-size: 14px;
  line-height: 17px;
  align-items: center;
  text-transform: uppercase;
  color: #3C444C;
}
.h1bg4{
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: 600;
  font-size: 44px;
  line-height: 56px;
  /* or 127% */
  text-align: center;
}
.h2bg4{
  font-family: Montserrat;
  font-style: normal;
  font-weight: 500;
  font-size: 19px;
  line-height: 158.47%;
  /* or 30px */
  text-align: center;
  opacity:0.8;
}
.triangleright{
  position:relative;
  left:50vw;
  
  transform: translate(0px, 0.11vw);
  width: 0; 
  height: 0; 
  border-left: 50vw solid transparent;
  border-right: 0px solid transparent;
  overflow: hidden;
  border-bottom: 4vw solid white;
}
.icon{
 font-size:  64px;
}
vantagens{
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: 500;
  font-size: 44px;
  line-height: 56px;
  color:black !important;
}
vantagens.titulo{
  font-family: Zilla Slab;
  font-style: normal;
  font-size: 24px;
  line-height: 28px;
  /* identical to box height, or 117% */

  text-align: center;

  color: #383837;
}
vantagens.subtitulo{
 font-family: Montserrat;
font-style: normal;
font-size: 14px;
line-height: 22px;
/* or 157% */

text-align: center;

color: #383837;
}
.bimage{
  background-image: url('../assets/bg2.png');
  background-size: cover;
  background-position:center bottom;
}
.contato{
  background-color: white;
  border-radius:10px;

}
.contato .h1{
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: 600;
  font-size: 36px;
  line-height: 56px;
  /* or 156% */

  text-align: center;

  color: #383837;
  color:black;
}
.contato .h3{
  font-family: Montserrat;
font-style: normal;
font-weight: 500;
font-size: 14px;
line-height: 158.47%;
/* or 22px */

text-align: center;

color: #383837;

opacity: 0.8;
}
@media only screen and (max-width: 500px) {
  .h1{
    font-size:32px !important;
  }
  .h2{
    font-size:16px !important;
  }
}
</style>