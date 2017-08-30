<template>
    <div id="price_cost">
        <div class="car_info">
            <span class="car_info_span car_info_span_1">车牌号：</span><span class="car_info_span car_info_span_1_">京A12345</span>
            <span class="car_info_span car_info_span_2">商业险折扣：</span><span class="car_info_span car_info_span_2_">京A12345</span>
            <span class="car_info_span car_info_span_3">车牌号：</span><span class="car_info_span car_info_span_3_">京A12345</span>
        </div>

    </div>
</template>

<script type="text/javascript">
    export default {
        name:"price_cost",
        data() {
            return{

            }

        },
        components:{

        },
        mounted() {

        },
        methods:{
        }
    }
</script>
<style scoped>
    #price_cost{
        width: 100%;
        height: 100%;
        background-color: #F8F8FF;

    }

    .car_info{
        width: 90%;
        height: 50px;
        display: inline-flex;
        border-radius: 10px;
        border: 1px solid #adadad;
        margin-top: 40px;
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
    .car_info_span{
        font-family: STKaiti;
        font-size: 18px;
        font-weight: 600;

        margin-top: 15px;
    }
    .car_info_span_1{
        margin-left: 20px;
    }
    .car_info_span_2{
        margin-left: 50px;
    }
    .car_info_span_3{
        margin-left: 60px;
    }




</style>