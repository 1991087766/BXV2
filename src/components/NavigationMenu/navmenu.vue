<template>
    <div id="navmenu">
        <div class="menudiv_up">
            <li ref="dom" class="actives" v-for="lys in ly" @click="selected_see(lys)" :class="{changeColor: activeName == lys}" >
                <img class="icon_l" src="/static/iconfont/attention_forbid.png">
                <span v-if="hide" class="nm_span"style="margin-top: 3px" >{{lys}}</span>
            </li>
            <li id="li_2" v-for="name in nm" :to="{path:name.path}" tag="li" class="actives"  @click="selected(name,name.path)" :class="{changeColor: activeName == name}">
                <img class="icon_l" v-bind:src="name.icon">
                <span v-if="hide" class="nm_span" >{{name.name}}</span>
            </li>
        </div>

        <div class="Other">
            <li id="li_3" v-for="p in products"  tag="li" class="actives" v-if="p.display" @click="selected(p,p.path)" :class="{changeColor: activeName == p}">
                <img class="icon_l" v-bind:src="p.icon">
                <span v-if="hide" class="nm_span" >{{p.name}}</span>
            </li>
        </div>


    </div>
</template>

<script type="text/javascript">
    export default {
        name: "navmenu",
        data(){
            return {
                willShow: true,
                hide:true,
                activeName: '',
                ly:['<<<<<<'],
                nm:[
                    {
                        name: '主 页',
                        path: '/home/page',
                        active: false,
                        icon:"/static/iconfont/home.png"
                    },
                    {
                        name: '报价出单',
                        path: '/home/price',
                        active: false,
                        icon:"/static/iconfont/sponsor.png"
                    },
                    {
                        name: '预约管理',
                        path: '/home/page',
                        active: false,
                        icon:"/static/iconfont/profile.png"
                    },
                    {
                        name: '客户管理',
                        path: '/home/CustomerMsz',
                        active: false,
                        icon:"/static/iconfont/group_fill.png"
                    }
                ],
                products: [
                    {
                        name: '客户资料',
                        path: '/home/CustomerMA',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/calendar.png"
                    },
                    {
                        name: '对账管理',
                        path: '/home/page',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/money_bag_fill.png"
                    },
                    {
                        name: '信息报表',
                        path: '/home/page',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/rank_fill.png"
                    },
                    {
                        name: '日志管理',
                        path: '/home/page',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/text.png"
                    },
                    {
                        name: '登录定位',
                        path: '/home/page',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/location_fill.png"
                    },
                    {
                        name: '部门管理',
                        path: '/home/StaffManagement',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/friend_fill.png"
                    },
                    {
                        name: '区域管理',
                        path: '/home/page',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/diqiu.png"
                    },
                    {
                        name: '系统管理',
                        path: '/home/page',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/setting.png"
                    },
                    {
                        name: '个人中心',
                        path: '/home/personal',
                        active: false,
                        display:true,
                        icon:"/static/iconfont/people_fill.png"
                    }
                ]

            }
        },
        methods: {
            fn: function () {
                if (this.willShow === true) {
                    this.willShow = false;
                } else {
                    this.willShow = true
                }
            },
            position: function (position) {
                this.$store.commit('setPosition', position);
                console.log(position);
                console.log(this.$store.state.position);
            },

            getAdmin(){
                if (this.getCookie("admin") === 2) {
                    return true
                } else {
                    return false
                }
            },

            getCookie(cname) {
                let name = cname + "=";
                let ca = document.cookie.split(';');
                for (let i = 0; i < ca.length; i++) {
                    let c = ca[i];
                    while (c.charAt(0) === ' ') c = c.substring(1);
                    if (c.indexOf(name) !== -1) return c.substring(name.length, c.length);
                }
                return "";
            },
            selected_see: function(gameName) {
                this.activeName = gameName
                if (this.hide === true) {
                    this.hide = false;
                } else {
                    this.hide = true
                }
//                this.$refs.dom.style.width = "24px";

            },
            selected: function(gameName,path) {
                this.activeName = gameName;
                this.$router.push(path);
            },
            demo(){
//                li_3
            }

        }
    }
</script>

<style scoped>
    #navmenu {
        font-family: "STKaiti";
        font-weight: bold;
        font-size: 20px;
        width: 100%;
        height: 100%;
        float: left;
    }
    .menudiv_up{
        display: grid;
        margin-left: 5px;
    }

    .Other {
        width: 100%;
        bottom: 15px;
        position: absolute;
        display: grid;
        margin-left: 5px;
    }



    li {
        width: 111px;
        /*width: 24px;*/
        /*margin-left: px;*/
        float: left;
        list-style-type: none;
        border-radius: 10px;
    }
    .actives{
        margin-top: 10px;
        /*margin-left: 5px;*/
        float: left;
        display: inline-flex;
    }
    .nm_span{
        margin-left: 5px;
        /*margin-top: 10px;*/
    }

    .icon_l{
        width: 23px;
        height:23px;
        /*margin-top: 8px;*/
        /*margin-left: 3px;*/
    }
    .icon_r{
        width: 16px;
        height:16px;
        margin-top: 2px;
        margin-right: 5px;
        float: right;
    }
    .changeColor{
        background-color: #07b843;
    }

</style>
