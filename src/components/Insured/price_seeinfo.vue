<template>
    <div id="price_search">
        <div class="car_info">
            <img class="cars_sign" src="/static/cars_sign/BMW.png"/>
            <div class="cars_info cars_info_1">
                <div class="cars_info_div">投保车型：
                    <span style="margin-right: 15px">
                        宝马
                    </span>
                    <input class="cars_info_div_btn btn" type="button"  value="点击此处修改车辆信息" >
                </div>
                <div class="cars_info_div">车辆识别代号：
                    <span>

                    </span>
                </div>
            </div>
            <div class="cars_info cars_info_2">
                <div class="cars_info_div">车主：
                    <span >

                    </span>
                </div>
                <div class="cars_info_div">发动机号：
                    <span>

                    </span>
                </div>
            </div>
        </div>
        <div class="car_info car_classify">
            <div class="cars_info cars_info_1 car_classify_1">
                <div class="car_classify_div">
                    <img class="car_classify_img" src="../../assets/iconfont/car_classify.png"/>
                    <span class="car_classify_div_span">选择车型</span>
                    <select class="search_input_span_input_1" name="select2" id="select_k1">
                        <option value="ALL" selected>-全部-</option>
                    </select>
                </div>
                <div class="car_classify_div">
                    <img class="car_classify_img" src="../../assets/iconfont/car_classify.png"/>
                    <span class="car_classify_div_span">使用性质</span>
                    <select class="search_input_span_input_1" name="select2" id="select_k2">
                        <option value="ALL" selected>-全部-</option>
                    </select>
                </div>
            </div>
            <div class="cars_info cars_info_2 car_classify_2">
                <div class="car_classify_div">
                    <img class="car_classify_img" src="../../assets/iconfont/car_classify.png"/>
                    <span class="car_classify_div_span">燃料种类</span>
                    <select class="search_input_span_input_1" name="select2" id="select_k3">
                        <option value="ALL" selected>-全部-</option>
                    </select>
                </div>
                <div class="car_classify_div">
                    <img class="car_classify_img" src="../../assets/iconfont/car_classify.png"/>
                    <span class="car_classify_div_span">投保类型</span>
                    <select class="search_input_span_input_1" name="select2" id="select_k4">
                        <option value="ALL" selected>-全部-</option>
                    </select>
                </div>
            </div>
        </div>
        <div class="car_info insurance">
            <table class="insurance_table" >
                <tbody>
                    <tr>
                        <td style="width: 20%"  class="td_l">
                            交强险/车船税
                        </td>
                        <td style="width: 30%">

                        </td>
                        <td>
                        </td>
                        <td style="width: 25%">

                        </td>
                        <td style="width: 15%">
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree1" name="check" checked />
                                <label for="slideThree1"></label>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td >

                        </td>
                        <td class="td_l">
                            已完税
                        </td>
                        <td >

                        </td>
                        <td >

                        </td>
                        <td >
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree2" name="check" checked />
                                <label for="slideThree2"></label>
                            </div>
                        </td>

                    </tr>
                    <tr>
                        <td style="width: 20%"  class="td_l">
                            商业险
                        </td>
                        <td style="width: 30%">

                        </td>
                        <td>
                        </td>
                        <td style="width: 15%">

                        </td>
                        <td style="width: 15%">
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree3" name="check" checked />
                                <label for="slideThree3"></label>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            机动车辆损失险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                            <span class="td_4_span">不计免赔</span>
                            <div class="slideThree slideThree_2">
                                <input type="checkbox" value="None" id="slideThree4" name="check" checked />
                                <label for="slideThree4"></label>
                            </div>
                        </td>
                        <td >
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree5" name="check" checked />
                                <label for="slideThree5"></label>
                            </div>
                        </td>

                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            第三者责任险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                            <span class="td_4_span">不计免赔</span>
                            <div class="slideThree slideThree_2">
                                <input type="checkbox" value="None" id="slideThree6" name="check" checked />
                                <label for="slideThree6"></label>
                            </div>
                        </td>
                        <td >
                            <select class="select_td" id="select_td_1">
                                <option value="ALL" selected>-全部-</option>
                            </select>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            司机险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                            <span class="td_4_span">不计免赔</span>
                            <div class="slideThree slideThree_2">
                                <input type="checkbox" value="None" id="slideThree7" name="check" checked />
                                <label for="slideThree7"></label>
                            </div>
                        </td>
                        <td >
                            <select class="select_td" id="select_td_2">
                                <option value="ALL" selected>-全部-</option>
                            </select>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            乘客险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                            <span class="td_4_span">不计免赔</span>
                            <div class="slideThree slideThree_2">
                                <input type="checkbox" value="None" id="slideThree8" name="check" checked />
                                <label for="slideThree8"></label>
                            </div>
                        </td>
                        <td >
                            <select class="select_td" id="select_td_3">
                                <option value="ALL" selected>-全部-</option>
                            </select>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            盗抢险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                            <span class="td_4_span">不计免赔</span>
                            <div class="slideThree slideThree_2">
                                <input type="checkbox" value="None" id="slideThree9" name="check" checked />
                                <label for="slideThree9"></label>
                            </div>
                        </td>
                        <td >
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree10" name="check" checked />
                                <label for="slideThree10"></label>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            玻璃险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                        </td>
                        <td >
                            <select class="select_td" id="select_td_5">
                                <option value="ALL" selected>-全部-</option>
                            </select>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            划痕险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                            <span class="td_4_span">不计免赔</span>
                            <div class="slideThree slideThree_2">
                                <input type="checkbox" value="None" id="slideThree11" name="check" checked />
                                <label for="slideThree11"></label>
                            </div>
                        </td>
                        <td >
                            <select class="select_td" id="select_td_6">
                                <option value="ALL" selected>-全部-</option>
                            </select>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            自燃险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                        </td>
                        <td >
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree12" name="check" checked />
                                <label for="slideThree12"></label>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            涉水险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                        </td>
                        <td >
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree13" name="check" checked />
                                <label for="slideThree13"></label>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td >
                        </td>
                        <td class="td_l">
                            机动车损失无法找到第三方险
                        </td>
                        <td >
                        </td>
                        <td class="td_4">
                        </td>
                        <td >
                            <div class="slideThree">
                                <input type="checkbox" value="None" id="slideThree14" name="check" checked />
                                <label for="slideThree14"></label>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td style="height: 15px">
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="btn_div">
            <input class="cars_info_div_btn btn btn_input_1 " type="button"  value="上一步" >
            <!--<input class="cars_info_div_btn btn" type="button"  value="点击此处修改车辆信息" >-->
            <input class="cars_info_div_btn btn btn_input_2" type="button"  value="下一步" >
        </div>
    </div>
</template>
<script type="text/javascript">
    export default {
        name:"price_search",
        data() {
            return{

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
    .car_info{
        margin-top: 40px;
        width: 90%;
        height: 120px;
        display: inline-flex;
        border-radius: 10px;
        border: 1px solid #adadad;
    }
    .cars_sign{
        width: 90px;
        height: 90px;
        margin-top: 15px;
        margin-left: 4%;
        display: block;
    }
    .cars_info{
        height: 80px;
        margin-top: 20px;
    }
    .cars_info_1{
        width: 40%;
        margin-left: 4%;

    }
    .cars_info_2{
        width: 30%;
        margin-left: 6%;
    }
    .cars_info_div{
        margin-top: 10px;
        font-weight: bold;
        font-family: STKaiti;
        font-size: 20px;
        display: table;
    }
    .cars_info_div_btn{
        width: 170px;
        height: 30px;
        background-color: #5cb85c;
        border: 1px solid #eeeeee;

    }

    .car_classify{
        margin-top: 20px;
        height: 140px;
    }
    .car_classify_1{
        margin-left: 3%;
        width: 45%;
        height: 100px;
    }
    .car_classify_2{
        margin-left: 3%;
        width: 45%;
        height: 100px;
    }

    .car_classify_div{
        display: inline-flex;
    }
    .car_classify_div_span{
        margin-top: 15px;
        margin-left: 10px;
        font-weight: bold;
        font-family: STKaiti;
        font-size: 18px;

    }
    .car_classify_img{
        width: 40px;
        height: 40px;
        margin-top: 5px;
    }

    .insurance{
        margin-top: 20px;
        margin-bottom: 20px;
        height: auto;
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
        height: 50px;
    }
    .td_4{
        display: inline-flex;
    }
    .td_4_span{
        margin-top: 15px;
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