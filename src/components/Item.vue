<template>
    <div>
        <div class="title">{{item.title}}
            <span class="time">4 小时前</span>
        </div>
        <div class="info" v-show="item.show">
            {{item.info}}
        </div>
        <hr v-show="isLast"/>
    </div>
</template>

<script>
    export default {
        name: 'Item',
        props: ['item', 'isLast']
    }

</script>

<style scoped>
    .title {
        font-size: 16px;
        line-height: 1.56em;
        color: #545454;
        font-weight: 500;
        position: relative;
        cursor: pointer;
        -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
    }
    
    .time {
        margin-left: 10px;
        font-size: 10px;
        color: #aaacb4;
    }
    
    .info {
        margin-top: 5px;
        font-size: 14px;
        line-height: 1.8em;
        color: #aaacb4;
    }
    
    hr {
        margin-top: 15px;
        margin-bottom: 15px;
        border: 1px solid #fff;
        position: relative;
    }
    
    hr:after {
        content: "";
        position: absolute;
        left: 0;
        bottom: 0;
        background: #ddd;
        width: 100%;
        height: 1px;
    }
</style>