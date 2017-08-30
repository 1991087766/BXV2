<template>
  <div id="home-header">
    <div id="title">IMS平台<span id="version">V0.0.1</span></div>
    <div id="setting">
      <span @click="devices()" class="name">
        {{uName}}
      </span>
      <img class="icon_user" src="../../assets/iconfont/usefull_fill.png"/>
      <!--　( <router-link to="/home/news"  tag="a"active-class="active">{{news}}</router-link> )-->
    </div>
  </div>

</template>

<script type="text/javascript">
export default {
  name:"header",
  data(){
    return{
      uName:"未登录",
      news:0
    }
  },
  created(){
        this.news=this.$store.state.news
  },
  mounted(){
      if(this.$store.state.uName!==null&&this.$store.state.uName===this.getCookie("NAME")){
        this.$store.commit("setUName",this.getCookie("NAME"));
        this.uName=this.getCookie("NAME")
      }else {
        if(this.getCookie("NAME")!==null){
          this.$store.commit("setUName",this.getCookie("NAME"));
          this.uName=this.getCookie("NAME")
        }else {
          this.uName="未登录"
        }
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
      return null;
    },
    devices:function(){
      this.$router.push('./Setting')
    }
  }
}
</script>

<style>
#home-header{
  height: 40px;
  font-family: "STKaiti";
  font-weight: bold;
  color: #F8F8FF;
  /*background: #191970;*/
  background: #191970;
}
#title{
  float: left;
  margin-top: 2px;
  margin-left: 15px;
  font-size: 35px;
}
#version{
  margin-left: 10px;
  margin-right: 10px;
  font-size: 20px;
}
#setting{
  width: 150px;
  height: 40px;
  float: right;
  margin-top: 10px;
  margin-right: 20px;
  font-size: 20px;
}
.icon_user{
  transform:rotate(180deg);
  margin-top: 5px;
  width: 15px;
  height: 10px;
}

</style>
