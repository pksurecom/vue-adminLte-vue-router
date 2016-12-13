<template>
    <ul class="sidebar-menu">
        <li class="header">工作台</li>
        <li class="active">
            <router-link :to="{ path:'/' }">
              <i class="glyphicon glyphicon-home"></i> <span>首页</span>
            </router-link>
        </li>
        <li class="treeview" v-for="item in items">
            <a href="#">
                <i class="fa fa-files-o"></i>
                <span>{{item.name}}</span>
                <span class="pull-right-container">
                    <i class="fa fa-angle-left pull-right"></i>
                </span>
            </a>
            <ul class="treeview-menu" v-if="item.sub.length>0">
                <li v-for="su in item.sub">
                    <router-link to="server_setting"><i class="fa fa-circle-o"></i>{{su.name}}</router-link>
                </li>
            </ul>
        </li>
    </ul>
</template>
<script>
    export default{
        name: 'left-menu',
        data(){
            return{
                items: []
            }
        },
        created(){
            this.$http.get('/menus').then((res) => {
                this.items = res.data.data.menus;
                console.log(this.items[0].sub.length>0);
            })
        }
    }
</script>
