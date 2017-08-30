<template>
    <div id="price_company">
        <div class="price_company_div">
            <span class="price_company_span">
                请选择投保公司(允许多选):
            </span>
        </div>
        <div class="car_info company">
            <div class="company_list">
                <div class="company_dev" v-for="l in list">
                    <img class="dev_img" :src="l.img"/>
                    <span class="company_dev_span">{{l.name}}</span>
                    <div class="slideThree">
                        <input type="checkbox" value="None" id="slideThree1" name="check" checked />
                        <label for="slideThree1"></label>
                    </div>
                    <div class="company_dev_d" v-if="l.display">去年投保</div>
                </div>
            </div>
            <div class="company_list2">
                <div class="company_dev" v-for="l in list">
                    <img class="dev_img" :src="l.img"/>
                    <span class="company_dev_span">{{l.name}}</span>
                    <div class="slideThree">
                        <input type="checkbox" value="None" id="slideThree2" name="check" checked />
                        <label for="slideThree2"></label>
                    </div>
                    <div class="company_dev_d" v-if="l.display">去年投保</div>
                </div>
            </div>
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
        name:"price_company",
        data() {
            return{
                list:[
                    {
                        img:"/static/baoxian/pingan.png",
                        name:"平安保险",
                        display:false,
                    },
                    {
                        img:"/static/baoxian/remmin.png",
                        name:"测试",
                        display:false,
                    },
                    {
                        img:"../../assets/iconfont/car_number.png",
                        name:"测试",
                        display:true,
                    },
                    {
                        img:"/static/baoxian/remmin.png",
                        name:"测试",
                        display:false,
                    },
                    {
                        img:"/static/baoxian/remmin.png",
                        name:"测试",
                        display:false,
                    }
                ]
            }
        }
    }
</script>
<style scoped>
    #price_company{
        width: 100%;
        height: 100%;
        background-color: #F8F8FF;
        overflow-y: auto;
    }
    .price_company_div{
        margin-top: 20px;
        width: 90%;
        display: inline-flex;
    }
    .price_company_span{
        display: flex;
    }
    .car_info{
        margin-top: 10px;
        width: 90%;
        height: 120px;
        display: inline-flex;
        border-radius: 10px;
        border: 1px solid #adadad;
    }
    .cars_info_div_btn{
        width: 170px;
        height: 30px;
        background-color: #5cb85c;
        border: 1px solid #eeeeee;

    }

    .company{
        margin-top: 10px;
        margin-bottom: 20px;
        height: 700px;
        overflow-x: auto;
        display: inline-block;
    }

    .company_dev{
        width: 100px;
        height: 250px;
        margin-top: 50px;
        margin-left: 6%;
        margin-right: 6%;
    }

    .company_list{
        width: 100%;
        display: inline-flex;
    }
    .company_list2{
        width: 100%;
        /*margin-top: 50%;*/
        display: inline-flex;
    }

    .dev_img{
        width: 100px;
        height: 100px;
    }

    .company_dev_d{
        margin-left: 10px;
        margin-top: 10px;
        background-color: #5cb85c;
        border-radius: 10px;
        font-family: STKaiti;
        font-weight: bold;
        color: #eeeeee;
        height: 20px;
    }
    .company_dev_span{
        margin-top: 10px;
        font-family: STKaiti;
        font-weight: bold;
        font-size: 20px;
        display: inherit;
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


    .slideThree {
        width: 80px;
        height: 26px;
        margin-top: 10px;
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