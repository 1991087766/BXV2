<template>
    <div id="price_search">

        <div class="Primer Primer1">
            <span class="title_">险种价格</span>
            <div class="Primer_a">
                <table class="insurance_table" >
                    <tbody>
                    <tr v-for="l in list">
                        <td style="width: 100px"  class="td_l">
                            <img class="td_img" :src="l.icon"/>
                        </td>
                        <td style="width: 17%">
                            <span class="td_span">
                                {{l.name}}
                            </span>
                        </td>
                        <td>
                            <div class="td_div_tb" v-if="l.past">去年投保</div>
                        </td>
                        <td>
                        </td>
                        <td style="width: 8%">
                            {{l.price}}
                        </td>
                        <td style="width: 100px">
                            <img class="td_img_del" src="../../assets/iconfont/policy.png"/>
                        </td>
                    </tr>

                    <tr>
                        <td style="height: 15px">
                        </td>
                    </tr>
                    </tbody>
                </table>
            </div>
        </div>

        <div class="Primer Primer2">
            <span class="title_">商业险/交强险日期</span>
            <div class="Primer_a">
                <table class="insurance_table">
                    <tbody>
                        <tr>
                            <td class="td_2" style="width: 15%">商业险日期</td>
                            <td class="td_2">商业险起保日期 <span class="time_span">{{price.s.start}}</span> （距离到期还有 <span class="time_span">{{price.s.end}}</span> 天）</td>
                            <td class="td_2" style="width: 15%"><input class="cars_info_div_btn btn btn_input_3" type="button"  value="修 改" ></td>
                        </tr>
                        <tr>
                            <td class="td_2">交强险日期</td>
                            <td class="td_2">交强险起保日期 <span class="time_span">{{price.s.start}}</span> （距离到期还有 <span class="time_span">{{price.s.end}}</span> 天）</td>
                            <td class="td_2"><input class="cars_info_div_btn btn btn_input_3" type="button"  value="修 改" ></td>
                        </tr>
                    </tbody>
                </table>
            </div>

        </div>
        <div class="Primer3">
            <input class="cars_info_div_btn btn btn_input_1 " type="button"  value="上一步" >
            <input class="cars_info_div_btn btn btn_input_2" type="button"  value="下一步" >
        </div>
        <div class="alter" v-if="false">
            <div class="alter_1">
                <span class="title_">修改商业险投保日期</span>
                <div class="alter_2">
                    商业险起保日期：
                    <input class="input_2" type="date" placeholder="登记日期"><br>
                    商业险结束日期：
                    <input class="input_2" type="date" placeholder="登记日期"><br><br><br>
                    <input class="cars_info_div_btn btn btn_input_1 alter_2_btn" type="button"  value="取 消" >
                    <input class="cars_info_div_btn btn btn_input_2 alter_2_btn" type="button"  value="确 定" >
                </div>
            </div>
        </div>
        <div class="alter" v-if="false">
            <div class="alter_1">
                <span class="title_">修改交强险投保日期</span>
                <div class="alter_2">
                    交强险起保日期：
                    <input class="input_2" type="date" placeholder="登记日期"><br>
                    交强险结束日期：
                    <input class="input_2" type="date" placeholder="登记日期"><br><br><br>
                    <input class="cars_info_div_btn btn btn_input_1 alter_2_btn" type="button"  value="取 消" >
                    <input class="cars_info_div_btn btn btn_input_2 alter_2_btn" type="button"  value="确 定" >
                </div>
            </div>
        </div>
    </div>
</template>
<script type="text/javascript">
    export default {
        name:"price_search",
        data() {
            return{
                list:[
                    {
                        name:"平安保险",
                        icon:"/static/baoxian/pingan.png",
                        price:"3304.88",
                        past:true
                    },
                    {
                        name:"人民保险",
                        icon:"/static/baoxian/remmin.png",
                        price:"4304.88",
                        past:false
                    },
                    {
                        name:"太平洋保险",
                        icon:"/static/baoxian/pingan.png",
                        price:"3314.88",
                        past:false
                    },
                    {
                        name:"平安保险",
                        icon:"/static/baoxian/pingan.png",
                        price:"3304.88",
                        past:false
                    },
                    {
                        name:"人民保险",
                        icon:"/static/baoxian/remmin.png",
                        price:"4304.88",
                        past:false
                    },
                    {
                        name:"太平洋保险",
                        icon:"/static/baoxian/pingan.png",
                        price:"3314.88",
                        past:false
                    }
                ],
                price:{
                    s:{
                        start:123456,
                        end:345678
                    },
                    j:{
                        start:123456,
                        end:345678
                    }
                }
            }
        }
    }
</script>
<style scoped>
    #price_search{
        width: 100%;
        height: 100%;
        background-color: #F8F8FF;
        overflow-y: auto;
    }
    .Primer{
        width: auto;
        border-radius: 5px;
        border: 1px solid #1cdde6;
        background-color: #1CDDE6;
        position: absolute;
    }
    .Primer1{

        height: 50%;
        top: 5%;
        left: 6%;
        right: 6%;
    }
    .Primer2{

        border: 1px solid #D0D35C;
        background-color: #D0D35C;
        height: 20%;
        top: 57%;
        left: 6%;
        right: 6%;
    }
    .Primer3{
        width: auto;
        position: absolute;
        height: 50px;
        top: 79%;
        left: 6%;
        right: 6%;
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

        overflow-y: auto;
    }
    .title_{
        margin-left: 10px;
        display: flex;
        font-family: STKaiti;
        font-size: 24px;
        font-weight: bold;
        color: #148b96;
    }
    .cars_info_div_btn{
        width: 170px;
        height: 30px;
        background-color: #5cb85c;
        border: 1px solid #eeeeee;

    }

    tbody{
        margin-bottom: 20px;
    }
    .insurance_table{
        width: 94%;
        margin-left: 3%;
        margin-top: 20px;
    }
    td{
        text-align: left;
        height: 100px;
        font-size: 23px;
        font-family: STKaiti;
        font-weight: bold;
    }
    .td_2{
        height: 50px;
    }
    .td_img{
        width: 80px;
        height: 80px;
    }
    .td_img_del{
        width: 50px;
        height: 50px;
        margin-left: 20px;
    }
    .td_div_tb{
        width: 81px;
        height: 24px;
        font-size: 20px;
        border-radius: 5px;
        background-color: #5cb85c;
        color: #eeeeee;
    }

    .time_span{
        color: #ff3622;
    }

    .alter{
        width: 100%;
        height: 100%;
        position: absolute;
        background-color: #888888;
        opacity: 0.9;
    }
    .alter_1{
        margin-top: 10%;
        margin-left: 27%;
        width: 600px;
        height: 250px;
        background-color: #6bff7a;
        border-radius: 10px;
    }
    .alter_2{
        margin-top: 5px;
        width: 600px;
        height: 250px;
        border-radius: 0 0 10px 10px;
        background-color: #F8F8FF;
    }



    .input_2{
        margin-top: 30px;
        font-weight: 600;
        font-size: 13px;
        font-family: STKaiti;
        border: 2px solid #CDC9C9;
        border-radius: 5px;
        width: 150px;
        height: 25px;
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
        border-radius: 10px;
        color: #fff;
        font-size: 15px;
        font-family: STKaiti;
        font-weight: bold;
    }

    .btn_div{
        margin-bottom: 40px;
    }
    .btn_input_1{
        height: 40px;
        font-size: 20px;
        background-color: #20a0ff;
    }
    .btn_input_2{
        height: 40px;
        font-size: 20px;
        margin-left: 200px;
    }
    .btn_input_3{
        width: 120px;
        height: 40px;
        font-size: 20px;
        background-color: #ff431e;
    }
    .alter_2_btn{
        margin-left: 30px;
    }
    select{
        width: 250px;
        height: 38px;
        font-size: 16px;
        font-family: STKaiti;
        border-radius: 10px;
        margin-left: 30px;
        margin-top: 5px;
    }
    .select_td{
        width: 80px;
        height: 25px;
        margin-left: 15px;
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
    .slideThree_2{
        margin-top: 13px;
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