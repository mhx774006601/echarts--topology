# echarts--topology
echarts实现的数据结构拓扑图


//根据窗口的大小变动 图表
			window.onresize = function(){
				myChart.resize();
			}
      
      
    //使用layui实现点击节点弹窗
		layui.use(['layer',], function(){
			  var layer = layui.layer
			//节点点击事件
			 myChart.on("click", jobrelation);
			 function jobrelation(){
			 	console.log('jobrelation');
			 	layer.open({
			 		type:2,
			 		title:'作业',
			 		maxmin: true,
			 		area:['1000px','500px'],
			 		content: 'job-simple.html'
			        ,btn: ['关闭'] 
			        ,yes: function(){
			          layer.closeAll(); 
			        }
			        
			 	})
			 }
  		});
