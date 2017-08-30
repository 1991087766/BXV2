<template>
    <div id="mypage">
        <div class="Primer">
            <span class="title_">主 页</span>
            <div class="Primer_a">
                <index v-if="true"></index>
            </div>
        </div>
    </div>
</template>

<script type="text/javascript">
    import index from './index.vue'
    export default {
        name:"mypage",
        data() {
            return{

            }

        },
        components:{
            index
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
<style scoped>
    #mypage{
        width: 100%;
        height: 100%;
        background-color: #F8F8FF;

    }
    .Primer{
        width: auto;
        height: auto;
        top: 8px;
        bottom: 8px;
        left: 8px;
        right: 8px;
        border-radius: 5px;
        border: 1px solid #6851c0;
        background-color: #6851c0;
        position: absolute;
    }
    .Primer_a{
        width: auto;
        height: auto;
        top: 30px;
        bottom: 1px;
        left: 1px;
        right: 1px;
        background-color: #F8F8FF;
        position: absolute;
    }
    .title_{
        margin-left: 10px;
        display: flex;
        font-family: STKaiti;
        font-size: 24px;
        font-weight: bold;
        color: #F8F8FF;
    }




</style>