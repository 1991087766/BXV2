<template>
    <div id="price_search">
        <div class="search">
            <div class="search_ search_1">
                <div class="search_title">
                    <span class="search_1_span">
                        方式一:根据车牌号投保查询
                    </span>
                    <div class="slideThree">
                        <input type="checkbox" value="None" id="slideThree1" name="check" checked />
                        <label for="slideThree1"></label>
                    </div>
                </div>
                <div class="search_input">
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/car_number.png"/>
                        <span class="search_input_span">
                            车牌号码
                        </span>
                        <input class="search_input_span_input search_input_span_input_1" type="text" placeholder="请输入车牌号码">
                    </div>
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/cae_n_c.png"/>
                        <span class="search_input_span">
                            号牌种类
                        </span>
                        <select class="search_input_span_input_1" name="select2" id="select_k1">
                            <option value="ALL" selected>-全部-</option>
                        </select>
                    </div>
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/car_classify.png"/>
                        <span class="search_input_span">
                            车辆种类
                        </span>
                        <select class="search_input_span_input_1" name="select2" id="select_k2">
                            <option value="ALL" selected>-全部-</option>
                        </select>
                    </div>
                </div>
            </div>
            <div class="search_ search_2">
                <div class="search_title">
                    <span class="search_1_span">
                        方式一:根据车牌号投保查询
                    </span>
                    <div class="slideThree">
                        <input type="checkbox" value="None" id="slideThree2" name="check" checked />
                        <label for="slideThree2"></label>
                    </div>
                </div>
                <div class="search_input">
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/recognition.png"/>
                        <span class="search_input_span">
                            识别代号
                        </span>
                        <input class="search_input_span_input search_input_span_input_2" type="text" placeholder="请输入车辆识别代号">
                    </div>
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/engine.png"/>
                        <span class="search_input_span">
                            发动机号
                        </span>
                        <input class="search_input_span_input search_input_span_input_2 " type="text" placeholder="请输入发动机号">
                    </div>
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/car_classify.png"/>
                        <span class="search_input_span">
                            车辆种类
                        </span>
                        <select class="search_input_span_input_2" name="select2" id="select_k3">
                            <option value="ALL" selected>-全部-</option>
                        </select>
                    </div>
                </div>
            </div>
            <div class="search_ search_3">
                <div class="search_title">
                    <span class="search_1_span">
                        方式一:根据车牌号投保查询
                    </span>
                    <div class="slideThree">
                        <input type="checkbox" value="None" id="slideThree3" name="check" checked />
                        <label for="slideThree3"></label>
                    </div>
                </div>
                <div class="search_input">
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/policy.png"/>
                        <span class="search_input_span">
                            保单号码
                        </span>
                        <input class="search_input_span_input search_input_span_input_3" type="text" placeholder="请输入保单号">
                    </div>
                    <div class="search_input_list">
                        <img class="search_input_img" src="../../assets/iconfont/car_classify.png"/>
                        <span class="search_input_span">
                            车辆种类
                        </span>
                        <select class="search_input_span_input_3" name="select2" id="select_k4">
                            <option value="ALL" selected>-全部-</option>
                        </select>
                    </div>
                    <div class="search_input_list">
                        <img class="search_input_img"/>
                    </div>
                </div>
            </div>
            <div class="search_div">
                <input class="btn btn_1" type="button"  value="历史查询" >
                <input class="btn btn_2" type="button"  value="下一步" >

            </div>
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

    }

    .search{
        top: 8%;
        width: 100%;
        height: 800px;
        position: absolute;
    }
    .search_{
        display: inline-block;
        width: 395px;
        height: 250px;
        border-radius: 5px;
    }
    .search_1{
        background-color: #87CEEB;
        border: 2px solid #87CEEB;
    }
    .search_2{
        margin-left: 5px;
        background-color: #E9D6AA;
        border: 2px solid #E9D6AA;
    }
    .search_3{
        margin-left: 5px;
        background-color: #FFAEB9;
        border: 2px solid #FFAEB9;
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
        width: 100%;
        display: block;
        height: 214px;
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
        margin-left: 15px;
        margin-top: 5px;
        width: 40px;
        height: 40px;
    }
    .search_input_span{
        margin-top: 12px;
        margin-left: 5px;
        font-size: 22px;
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
        background-color: #5cb85c;
        border: 1px solid #5cb85c;
    }
    .btn_2{
        background-color: #20a0ff;
        border: 1px solid #20a0ff;
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