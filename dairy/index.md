---
title: 关于
layout: page
comments: no
---

{{ site.dairy }}


<head>
	<style>
		.over {position: fixed; left:0; top:0; width:100%; z-index:100;}
		.tempContainer {position:fixed; width:100%; margin-right:0px; margin-left:0px; text-align:center; z-index:101;}
		span{
				display:block;
			}
			.space {
				margin-bottom:50px;

	</style>


	<script src="http://code.jquery.com/jquery-1.8.0.min.js"></script>
</head>


<body>
	<script>
		$(document).ready(function () {
			var imgsObj = $('.amplifyImg img');//需要放大的图像
			if(imgsObj){
				$.each(imgsObj,function(){
					$(this).click(function(){
						var currImg = $(this);
						coverLayer(1);
						var tempContainer = $('<div class=tempContainer></div>');//图片容器
						with(tempContainer){//width方法等同于$(this)
							appendTo("body");
							var windowWidth=$(window).width();
							var windowHeight=$(window).height();
							//获取图片原始宽度、高度
							var orignImg = new Image();
							orignImg.src =currImg.attr("src") ;
							var currImgWidth= orignImg.width;
							var currImgHeight = orignImg.height;
							if(currImgWidth<windowWidth){//为了让图片不失真，当图片宽度较小的时候，保留原图
								if(currImgHeight<windowHeight){
									var topHeight=(windowHeight-currImgHeight)/2;
									if(topHeight>35){/*此处为了使图片高度上居中显示在整个手机屏幕中：因为在android,ios的微信中会有一个title导航，35为title导航的高度*/
										topHeight=topHeight-35;
										css('top',topHeight);
									}else{
										css('top',25);
									}
									html('<img border=0 src=' + currImg.attr('src') + '>');
								}else{
									css('top',25);
									html('<img border=0 src=' + currImg.attr('src') + ' height='+windowHeight*0.7+'>');
								}
							}else{
								var currImgChangeHeight=(currImgHeight*windowWidth)/currImgWidth;
								if(currImgChangeHeight<windowHeight){
									var topHeight=(windowHeight-currImgChangeHeight)/2;
									if(topHeight>35){
										topHeight=topHeight-35;
										css('top',topHeight);
									}else{
										css('top',25);
									}
									html('<img border=0 src=' + currImg.attr('src') + ' width='+windowWidth*0.7+';>');
								}else{
									css('top',25);
									html('<img border=0 src=' + currImg.attr('src') + ' width='+windowWidth*0.7+'; height='+windowHeight*0.7+'>');
								}
							}
						}
						tempContainer.click(function(){
							$(this).remove();
							coverLayer(0);
						});
					});
				});
			}
			else{
				return false;
			}
			//使用禁用蒙层效果
			function coverLayer(tag){
				with($('.over')){
					if(tag==1){
						css('height',$(document).height());
						css('display','block');
						css('opacity',1);
						css("background-color","#FFFFFF");
						css("background-color","rgba(0,0,0,0.7)" );  //蒙层透明度
					}
					else{
						css('display','none');
					}
				}
			}
		});
	</script>



	<div class="panel-body" style="height: 400px; width: 708px; overflow-y:scroll">
	<div style="border: 1px  #000000; width: 90%; margin: 0 auto;">
		<span  class = "space">
			<p>7月6日 17:02</p>
			<font  color="red">某些复杂决策环境下，选择它并不是因为它是最好的，而是因别无可选</font>
			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->
			<table><tr>
			<td><img src="liushiwen3.PNG" height="200*0.518" width="200" border=0 /></td>
			<td><img src="liushiwen3.PNG" height="200*0.518" width="200" border=0 /></td>
			<td><img src="liushiwen3.PNG" height="200*0.518" width="200" border=0 /></td>
			</tr></table>
			</div>

		</span>


		<span class = "space">

			<p>7月4日 21:15</p>
			<font  color="red">隔行听建议，本行靠自己。</font>

		</span>

	
