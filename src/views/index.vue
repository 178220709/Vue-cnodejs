<template>
    <!-- 全局header -->
    <nv-top></nv-top>

    <div style="text-align: center ; margin: 100px 0 0 0 ">
        <div class="container ">
            <p style="font-size: 30px">Please input the access code </p>

            <div style="margin: 30px 0 0 0 ">
                <div class="input-group col-sm-3 " style="margin: auto">
                    <input type="text" v-model="code" class="form-control" placeholder="access code">
                    <span class="input-group-addon" @click="checkClick">check</span>
                </div>
            </div>

        </div>
    </div>


</template>
<script type="text/babel">
    export default {
        data(){
            return {
                code: ""
            }
        },
        methods: {
            checkClick(){
                if (this.code && this.code == "json") {
                    alert("success");
                }else{
                    alert("error");
                }
            }
        },
        components: {
            'nvTop': require('../components/top.vue')
        }

    }
</script>
<style lang="sass">
    @import '../assets/bootstrap/css/bootstrap.css';

    .title {
        font-size: 30px;

    }
</style>

