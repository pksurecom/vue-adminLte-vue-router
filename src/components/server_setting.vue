<!-- attendance.vue -->
<template>
  <div class="content-wrapper">
    <!-- Content Header (Page header) -->
    <content-header v-bind:menuList="menuList"></content-header>

    <!-- Main content -->
    <section class="content">
      <div class="row">
        <div class="col-xs-12">
          <div class="box">
            <div class="box-header with-border">
                <div class="form-group">
                  <button class="btn btn-primary">添加</button>
                </div>
            </div>
            <!-- /.box-header -->
            <div class="box-body">
              <table class="table table-bordered">
                <thead>
                	<tr>
	                  <th>服务器ip</th>
	                  <th>http端口</th>
	                  <th>socket通信端口</th>
	                  <th>添加时间</th>
	                  <th>操作</th>
	                </tr>
                </thead>
                <tbody>
                	<tr>
	                  <td>192.168.1.201</td>
	                  <td>8080</td>
	                  <td>8423</td>
	                  <td>2016-12-14 20:00:00</td>
	                  <td>修改 | 删除</td>
	                </tr>
                </tbody>
              </table>
            </div>
            <!-- /.box-body -->
            <div class="box-footer clearfix">
              <ul class="pagination pagination-sm no-margin pull-right">
                <li><a href="#">&laquo;</a></li>
                <li><a href="#">1</a></li>
                <li><a href="#">2</a></li>
                <li><a href="#">3</a></li>
                <li><a href="#">&raquo;</a></li>
              </ul>
            </div>
          </div>
          <!-- /.box -->
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import contentHeader from './content_header'
export default {
  data() {
  	return {
        msg: '数据',
        menuList:[
        	{
        		text:"考勤管理",
        		isActive:false
        	},
        	{
        		text:"我的考勤记录",
        		isActive:true
        	}
        ],

    }
  },
  components: {
    contentHeader
  },
  mounted(){},
  methods: {}
}
</script>
