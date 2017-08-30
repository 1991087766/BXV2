<template>
  <div id="NavMenu">
    <NavMenuSalesman class="NavMenuSalesman" ></NavMenuSalesman>
  </div>
</template>

<script type="text/javascript">
import NavMenuSalesman from '../NavigationMenu/navmenu.vue'
export default {
  name:"NavMenu",
  components: {
      NavMenuSalesman
   },
  mounted() {
    if(this.getCookie("username")===null && this.getCookie("username")===""){
      this.$router.push('../login')
    }
  },
  methods:{
        getCookie(cname) {
            let name = cname + "=";
            let ca = document.cookie.split(';');
            for(let i=0; i<ca.length; i++) {
                let c = ca[i];
                while (c.charAt(0)===' ') c = c.substring(1);
                if (c.indexOf(name) !== -1) return c.substring(name.length, c.length);
            }
            return "";
        }
    }
}
</script>

<style>
#NavMenu{
  width: 125px;
  /*width: 35px;*/
  height: auto;
  background: #F8F8FF;
  position: fixed;
  float: left;
  top: 42px;
  left: 2px;
  bottom: 2px;
  /*border-radius: 5px;*/
}
  .NavMenuSalesman{
    /*display: none;*/
  }



</style>
