<template>
    <div class="home">
        <div class="header" id="top">
            <div class="logo1">
                <div class="log_img">
                    <img src="http://www.faw-hongqi.com.cn/pcs/images/logo.png" alt="">
                </div>
            </div>

            <div class="logo2">
                <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
                    <el-menu-item index="1" class="item"><a style="text-decoration: none" href="/"
                                                            target="_blank">首页</a></el-menu-item>

                    <el-menu-item index="2" class="item">车型产品</el-menu-item>
                    <el-menu-item index="3" class="item">服务支持</el-menu-item>
                    <el-menu-item index="4" class="item">优享金融</el-menu-item>
                    <el-menu-item index="5" class="item">品牌资讯</el-menu-item>
                </el-menu>
                <div class="line"></div>
            </div>
        </div>
        <!--      轮播图-->
        <div class="carousel">
            <el-carousel height="512px">
                <el-carousel-item v-for="item in images" :key="item.url">
                    <img :src="item.url" style="height: 512px;width: 1200px" alt="">
                </el-carousel-item>
            </el-carousel>
        </div>
        <!--      汽车详情-->
        <div class="center">
            <div><img src="http://www.faw-hongqi.com.cn/pcs/images/car/H5f.jpg??2020-07-10" alt=""></div>
            <div><img src="http://www.faw-hongqi.com.cn/pcs/images/car/H7f.jpg" alt=""></div>
            <div><img src="http://www.faw-hongqi.com.cn/pcs/images/car/H9f.jpg?n=2" alt=""></div>
            <div><img src="http://www.faw-hongqi.com.cn/pcs/images/car/lf.jpg" alt=""></div>
            <div><img src="http://www.faw-hongqi.com.cn/pcs/images/car/hs5f.jpg" alt=""></div>
            <div><img src="http://www.faw-hongqi.com.cn/pcs/images/car/hs7.jpg?n=2" alt=""></div>
            <div><img src="http://www.faw-hongqi.com.cn/pcs/images/car/L5f.jpg" alt=""></div>

        </div>
        <!--        图片-->
        <div class="imgs" v-for="item in imgs" :key="item.url">
            <img :src="item.url" alt="">
        </div>

        <!--        底部导航-->
        <footer>
            <div class="one">
                <div style="padding-left: 30px" class="tableBox">
                    <el-table
                            :data="tableData">

                        <el-table-column
                                prop="date"
                                label="车型产品"
                                width="180">
                        </el-table-column>
                        <el-table-column
                                prop="name"
                                label="服务支持"
                                width="180">
                        </el-table-column>
                        <el-table-column
                                prop="address"
                                label="优享金融">
                        </el-table-column>
                        <el-table-column
                                prop=""
                                label="经销商招募">
                        </el-table-column>
                        <el-table-column
                                prop=""
                                label="品牌资讯">
                        </el-table-column>
                    </el-table>
                    <!--            回到顶部-->
                    <a href="#top">
                        <div class="go-top">
                            <div style="display: flex;justify-content: center">
                                <img src="../../public/img/上箭头.png" alt="">
                            </div>
                            <div style="text-align: center;color: #575757;font-size: 13.33px">返回顶部:<br/>24小时全天候服务热线:
                                <br/>4008-171717</div>
                        </div>
                    </a>
                </div>
            </div>
            <div class="two">
                <div class="container">
                    <div class="first">
                        <a href="https://weibo.com/yiqihongqi?sudaref=www.baidu.com&retcode=6102&is_all=1" style="color: #575757;text-decoration: none">
                            <div class="wb" >
                                <div class="wb-img">
                                    <img src="http://www.faw-hongqi.com.cn/pcs/images/foot2_1_i2.png" alt="">
                                </div>
                                <div class="wb-text">官方微博</div>
                            </div>
                        </a>


                        <el-tooltip placement="top" effect="light">
                            <div slot="content">
                                <img src="../../public/img/二维码.png" style="width: 200px" alt="">
                            </div>

                            <div class="wx">
                                <div class="wx-img" >
                                    <img  src="http://www.faw-hongqi.com.cn/pcs/images/foot2_1_i3.png" alt="">
                                </div>
                                <div class="wx-text">官方微信</div>
                            </div>
                        </el-tooltip>
                    </div>
                    <div class="next">
                        <div>联系我们</div>
                        <div style="border-left: 1px solid #575757">网站声明</div>
                        <div style="border-left: 1px solid #575757">中国一汽</div>
                    </div>
                    <div class="last">
                        <div>2017中国第一汽车股份有限公司版权所有</div>
                        <div>吉ICP备09003045号</div>
                    </div>
                </div>
            </div>
            

        </footer>
    </div>
</template>

<script>
    export default {
        name: 'home',
        props: {
            msg: String
        },
        data() {
            return {
                tableData: [{
                    date: 'H5',
                    name: '服务理念',
                    address: '金融方案'
                }, {
                    date: 'H7',
                    name: '维修与保养',
                    address: '购车计算器'
                }, {
                    date: 'H9',
                    name: '服务网点',
                    address: ''
                }, {
                    date: 'E-HS3',
                    name: '',
                    address: ''
                }
                ],
                activeIndex: '1',
                activeIndex2: '1',
                images: [
                    {url: "http://www.faw-hongqi.com.cn/pcs/images/h5video1.jpg?n=1"},
                    {url: "http://www.faw-hongqi.com.cn/pcs/images/hb-banner.jpg?n2"},
                    {url: "http://www.faw-hongqi.com.cn/pcs/images/car/hs7banner.jpg?n=1"},
                    {url: "http://www.faw-hongqi.com.cn/pcs/images/car/HS5-pc_banner.jpg"},
                ],
                imgs: [
                    {url: 'http://www.faw-hongqi.com.cn/pcs/images/m2_img.jpg'},
                    {url: 'http://www.faw-hongqi.com.cn/pcs/images/m3_img.jpg'},
                    {url: 'http://www.faw-hongqi.com.cn/pcs/images/m4_img.jpg'},
                ]
            };
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }


        }

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "public/scss/index.scss";

    .el-table {
        /deep/ tbody tr:hover > td {
            background-color: white;
        }
    }

</style>
<style>

    .one .el-table td,
    .one .el-table th.is-leaf,
    .one .el-table--border,
    .one .el-table--group {
        border: none;
        cursor: pointer;
    }

    .one .el-table::before {
        height: 0;
    }

</style>
