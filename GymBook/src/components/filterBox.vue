<template>
    <div>
        <div class="reserveBox">
            <navigation></navigation>
            <div class="breadNav">
                <span>首页</span>
                <span>></span>
                <span>预定中心</span>
            </div>
            <div class="filterBox">
                <div class="searchBox">
                    <el-input placeholder="关键字"  size="small">
                        <template class="seacrchBtn" slot="append">搜索</template>
                    </el-input>
                </div>
                <div class="content">
                    <ul>
                        <li>预定类型
                            <span class="spanActive">全部</span>
                            <span>场地</span>
                        </li>
                        <li>所属校区
                            <span class="spanActive">全部</span>
                            <span>南校区</span>
                            <span>北校区</span>
                            <span>东校区</span>
                            <span>珠海校区</span>
                        </li>
                    </ul>
                </div>
            </div>
            <collect></collect>
        </div>
    </div>
</template>


<script>
    import navigation from '../components/navigation';
    import collect from '../components/collect';
    import { mapActions, mapState } from 'vuex';

    export default {
        data() {
           return {

           }
        },
        components: {
           navigation,
           collect    
        },
        methods: {
            ...mapActions([
                'getGym'
            ])
        }
    }
</script>
<style lang="scss" scoped type="text/css">
    .reserveBox {
        padding: 10px 15px 15px 15px;
        .breadNav {
            width: 100%;
            border-bottom: 2px solid #ddd;
            padding: 8px 0;
            span {
                font-size: 14px;
                color: #555;
            }
        }
        .filterBox {
            padding: 15px 0;
            .searchBox {
                width: 35%;
                .seacrchBtn {
                    cursor: pointer;
                }
            }
            el-input {
               
            }
        }
        .content {
            width: 100%;
            ul {
                width: 100%;
                padding: 0;
                li {
                    list-style-type: none;
                    line-height: 24px;
                    padding: 5px 0;
                    span {
                        display: inline-block;
                        padding: 1px 7px;
                        cursor: pointer;
                        margin: 0 5px;
                    }
                    span:hover {
                        background: blue;
                        color: #fff;
                    }
                    .spanActive {
                        background: blue;
                        color: #fff;
                    }
                }
            }
        }
    }
</style>

