<template>
    <div id="price_list">
        <div class="Primer">
            <span class="title_">报价出单</span>
            <div class="Primer_a">
                <price_search v-if="true"></price_search>
                <price_seeinfo v-if="false"></price_seeinfo>
                <price_company v-if="false"></price_company>
                <price_policy v-if="false"></price_policy>
                <price_cost v-if="false"></price_cost>
            </div>
        </div>

    </div>
</template>

<script type="text/javascript">
    import price_search from './price_search.vue'
    import price_seeinfo from './price_seeinfo.vue'
    import price_company from './price_i_c.vue'
    import price_policy from './price_policy.vue'
    import price_cost from './price_cost.vue'
    export default {
        name:"price_list",
        data() {
            return{

            }

        },
        components:{
            price_search,
            price_seeinfo,
            price_company,
            price_policy,
            price_cost
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
    #price_list{
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
        border: 1px solid #057c14;
        background-color: #057c14;
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