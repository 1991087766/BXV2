<template>
    <div id="index">
        <div class="search">
            <div class="search_ search_1">
                <div class="search_title">
                    <span class="search_1_span">
                        个人资料
                    </span>
                </div>
                <div class="search_input">
                    <div class="search_input_list" v-for="i,n in info_1" :title="icon_1[n]">
                        <img class="search_input_img" :src="'/static/iconfont/personal/'+icon_1[n]+'.png'"/>
                        <span class="search_input_span">
                            {{i}}
                        </span>
                    </div>
                </div>
            </div>
            <div class="search_ search_2">
                <div class="search_title">
                    <span class="search_1_span">
                        部门信息
                    </span>
                </div>
                <div class="search_input">
                    <div class="search_input_list" v-for="i,n in info_2" :title="icon_2[n]">
                        <img class="search_input_img" :src="'/static/iconfont/personal/'+icon_2[n]+'.png'"/>
                        <span class="search_input_span">
                            {{i}}
                        </span>
                    </div>
                </div>
            </div>
            <div class="search_ search_3">
                <div class="search_title">
                    <span class="search_1_span">
                        其 他
                    </span>
                </div>
                <div class="search_input">
                    <div class="search_input_list" v-for="i,n in info_3" :title="icon_3[n]">
                        <img class="search_input_img" :src="'/static/iconfont/personal/'+icon_3[n]+'.png'"/>
                        <span class="search_input_span">
                            {{i}}
                        </span>
                    </div>
                </div>
            </div>
            <div class="search_div">
                <input class="btn btn_1" type="button"  value="修改信息" >
                <input class="btn btn_2" type="button"  value="修改密码" >
                <input class="btn btn_3" type="button"  value="退出登录" >
            </div>
        </div>

    </div>
</template>
<script type="text/javascript">
    export default {
        name:"index",
        data() {
            return{
                info_1:['徐君基','男','15825507654','Navy_xu@sina.cn','浙江省杭州市西湖区西溪水岸花苑23栋2单元302'],
                info_2:['IMS-A0000100000','开发工程师','研发部','徐君基','浙江省杭州市'],
                info_3:['20170201','190天','5级','超级管理','正式员工'],
                icon_1:['姓名','性别','电话','邮箱','地址'],
                icon_2:['编号','职务','部门','Leader','网点'],
                icon_3:['入职日期','入职时长','控制等级','系统权限','是否正式员工']
            }
        }
    }
</script>
<style scoped>
    #index{
        width: 100%;
        height: 100%;
        background-color: #F8F8FF;

    }

    .search{
        top: 8%;
        width: 100%;
        height: 800px;
        position: absolute;
    }
    .search_{
        display: inline-block;
        width: 365px;
        height:400px;
        border-radius: 5px;
    }
    .search_1{
        background-color: #9bd522;
        border: 2px solid #9bd522;
    }
    .search_2{
        margin-left: 5px;
        background-color: #ffad2d;
        border: 2px solid #ffad2d;
        width: 320px;
    }
    .search_3{
        margin-left: 5px;
        background-color: #ff7cb8;
        border: 2px solid #ff7cb8;
        width: 320px;
    }
    .search_title{
        width: 100%;
        display: flex;

    }
    .search_1_span{
        margin-left: 10px;
        margin-top: 8px;
        font-size: 18px;
        font-weight: bold;
        font-family: STKaiti;
    }
    .search_input{
        margin-top: 10px;
        width: 100%;
        display: block;
        height: 364px;
        background-color: #F8F8FF;
    }

    .search_input_list{
        width: 100%;
        height: 50px;
        margin-top: 15px;
        display: inline-flex;
        /*background-color: #20a0ff;*/
    }
    .search_input_img{
        margin-left: 30px;
        margin-top: 5px;
        width: 40px;
        height: 40px;
    }
    .search_input_span{
        margin-top: 12px;
        margin-left: 20px;
        font-size: 20px;
        font-weight: bold;
        font-family: STKaiti;
    }
    .search_input_span_input{
        font-weight: 600;
        font-size: 16px;
        font-family: STKaiti;
        border-radius: 5px;
        width: 180px;
        height: 30px;
        margin-top: 5px;
        margin-left: 30px;
    }
    .search_input_span_input_1{
        border: 2px solid #87CEEB;
    }
    .search_input_span_input_2{
        border: 2px solid #E9D6AA;
    }
    .search_input_span_input_3{
        border: 2px solid #FFAEB9;
    }

    select{
        width: 185px;
        height: 38px;
        font-size: 16px;
        font-family: STKaiti;
        /*font-weight: bold;*/
        border-radius: 10px;
        margin-left: 30px;
        margin-top: 5px;
    }

    .search_div{
        margin-top: 50px;
        width: auto;
        height: 100px;
    }
    .btn{
        line-height: 1;
        white-space: nowrap;
        cursor: pointer;
        -webkit-appearance: none;
        text-align: center;
        box-sizing: border-box;
        outline: 0;
        margin: 0;
        padding: 7px 9px;
        border-radius: 10px;
        color: #fff;
        width: 100px;
        height: 40px;
        font-size: 20px;
        font-family: STKaiti;
        font-weight: bold;
    }
    .btn_1{
        background-color: #ff607b;
        border: 1px solid #ff607b;
    }
    .btn_2{
        background-color: #20a0ff;
        border: 1px solid #20a0ff;
        margin-left: 200px;
    }
    .btn_3{
        background-color: #941be7;
        border: 1px solid #941be7;
        margin-left: 200px;
    }

    .slideThree {
        width: 80px;
        height: 26px;
        margin-top: 5px;
        margin-bottom: 5px;
        margin-left: 15px;
        background: #333;
        position: relative;
        -moz-border-radius: 50px;
        -webkit-border-radius: 50px;
        border-radius: 50px;
        -moz-box-shadow: inset 0px 1px 1px rgba(0, 0, 0, 0.5), 0px 1px 0px rgba(255, 255, 255, 0.2);
        -webkit-box-shadow: inset 0px 1px 1px rgba(0, 0, 0, 0.5), 0px 1px 0px rgba(255, 255, 255, 0.2);
        box-shadow: inset 0px 1px 1px rgba(0, 0, 0, 0.5), 0px 1px 0px rgba(255, 255, 255, 0.2);
    }
    .slideThree:after {
        content: 'OFF';
        color: #F8F8FF;
        position: absolute;
        right: 10px;
        z-index: 0;
        font: 12px/26px Arial, sans-serif;
        font-weight: bold;
        text-shadow: 1px 1px 0px rgba(255, 255, 255, 0.15);
    }
    .slideThree:before {
        content: 'ON';
        color: #00bf00;
        position: absolute;
        left: 10px;
        z-index: 0;
        font: 12px/26px Arial, sans-serif;
        font-weight: bold;
    }
    .slideThree label {
        display: block;
        width: 34px;
        height: 20px;
        cursor: pointer;
        position: absolute;
        top: 3px;
        left: 3px;
        z-index: 1;
        background: #fcfff4;
        background: -moz-linear-gradient(top, #fcfff4 0%, #dfe5d7 40%, #b3bead 100%);
        background: -webkit-linear-gradient(top, #fcfff4 0%, #dfe5d7 40%, #b3bead 100%);
        background: linear-gradient(to bottom, #fcfff4 0%, #dfe5d7 40%, #b3bead 100%);
        -moz-border-radius: 50px;
        -webkit-border-radius: 50px;
        border-radius: 50px;
        -moz-transition: all 0.4s ease;
        -o-transition: all 0.4s ease;
        -webkit-transition: all 0.4s ease;
        transition: all 0.4s ease;
        -moz-box-shadow: 0px 2px 5px 0px rgba(0, 0, 0, 0.3);
        -webkit-box-shadow: 0px 2px 5px 0px rgba(0, 0, 0, 0.3);
        box-shadow: 0px 2px 5px 0px rgba(0, 0, 0, 0.3);
    }
    .slideThree input[type=checkbox] {
        visibility: hidden;
    }
    .slideThree input[type=checkbox]:checked + label {
        left: 43px;
    }



</style>