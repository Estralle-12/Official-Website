<template>
    <header class="top-container">
        <img src="../assets/cy-logo.png" class="logo" />
        <div class="topbar-nav">
            <ul class="nav-wrap">
                <li v-for="(item, i) in navs" class="nav" :key="i">
                    <template>
                        <a :href="item.sourceUrl" class="nav-name" target="_blank">{{ item.name }}</a>
                    </template>
                </li>
            </ul>
        </div>
        <div class="topbar-info">
            <a href="http://order.mi.com/site/login?redirectUrl=http://www.mi.com/index.html">登陆</a>
            <span class="nav-separate" v-show="$index !== 8">|</span>
            <a href="https://account.xiaomi.com/pass/register">注册</a>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            navs: [
                { name: '首页', sourceUrl: 'http://www.baidu.com' },
                { name: '简介', sourceUrl: 'http://www.baidu.com' },
                { name: '爱宠咨询', sourceUrl: 'http://www.baidu.com' },
                { name: '宠友圈', sourceUrl: 'http://www.baidu.com' },
                { name: '招商合作', sourceUrl: 'http://www.baidu.com' },
                { name: '加入我们', sourceUrl: 'http://www.baidu.com' },
                { name: '留言板', sourceUrl: 'http://www.baidu.com' },
                { name: '联系我们', sourceUrl: 'http://www.baidu.com' },
            ]
        }
    },
}
</script>

<style scoped>
.top-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 80%;
    height: 100px;
    /* background: #333; */
    background: #ffffff;
    margin: 0 auto;
}

.logo {
    height: 60px;
    margin-right: 130px;
}


.topbar-nav {
    margin-right: 200px;

    .nav-wrap {
        display: inline-block;
        margin: 0;
        padding: 0;
        list-style: none;

        .nav {
            display: inline-block;
            padding: 0 15px;

            & :hover {
                color: #fff;
            }

            .nav-name {
                display: inline-block;
                font-size: 16px;
                color: #2B2E2E;
                text-decoration: none;
            }

            .nav-name:hover {
                color: #0ad;
            }
        }
    }
}

.topbar-info {
    a {
        color: #2B2E2E;
        text-decoration: none;

        &:hover {
            color: #b0b0b0;
        }
    }

    span {
        color: #2B2E2E;
    }
}
</style>