---
title: 
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
		img{
				height="200*0.518";
				width="200" ;
				border=0
			}
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



	<div class="panel-body" style="height: 800px; width: 708px; overflow-y:scroll">
	<div style="border: 1px  #000000; width: 90%; margin: 0 auto;">

		<span  class = "space">
			<p>9月6日 17:43</p>
			<font  color="red">现在的预期管理和两三年前已大不相同了，以前是直接丢给你个炮仗就炸起来，现在是在你跟前点个引子告诉你：看，我要点了啊！    <a href="http://www.pbc.gov.cn/goutongjiaoliu/113456/113469/3886672/index.html" target="_blank"><font color="green">网页连接</font></a></font>

			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->

			</div>
		</span>
	
	
	
		<span  class = "space">
			<p>9月6日 16:56</p>
			<font  color="red">It definitely is!</font>
			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->
			<table><tr>
			<td><img src="https://raw.githubusercontent.com/wuyy2007/resouce/master/webcontentpic/qje_clip.png" height="103" width="200" margin="5" /></td>
			</tr></table>
			</div>
		</span>

		
	

		<span  class = "space">
			<p>8月25日 19:55</p>
			<font  color="red">非常有趣的是，中国的金融改革往往放在8月。至此，中国的利、汇、贷市场化迈出了重大一步。(尽管目前这种价格形成机制的特征仍是“人工+智能” 的形式)     <a href="http://www.pbc.gov.cn/goutongjiaoliu/113456/113469/3879648/index.html" target="_blank"><font color="green">网页连接</font></a></font>

			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->

			</div>
		</span>
	
	
	
	
		<span  class = "space">
			<p>8月24日 23:03</p>
			<font  color="red">理性人有偏见吗？理性人做的决策都正确吗？</font>
			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->

			</div>
		</span>
	
	



		<span  class = "space">
			<p>8月22日 23:58</p>
			<font  color="red">生个二胎给头胎做个伴，听起来似乎合理。但细想一下，这不足以作为生二胎的理由，尤其在头胎较大的时候更是站不住脚。其实是二胎获得了有伴的福利而非头胎，头胎被强制要学会腾出资源，要学会仍让。头胎的伴其实更需要的是来自父母而非弟妹。</font>
			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->

			</div>
		</span>
	
	
	

	
		<span  class = "space">
			<p>8月5日 11:51</p>
			<font  color="red">如果久跟央行外汇政策的话，今天这份人民币"破七"声明则显得比较特殊。印象之中，这是官方首次将贬值预期直接归因于美方责任，非常罕见。汇率本身或已被纳入对外政策工具箱，金融反击慢慢浮上水面。</font>
			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->
			<table><tr>
			<td><img src="https://raw.githubusercontent.com/wuyy2007/resouce/master/webcontentpic/pboc_rmb.jpg" height="100" width="70" margin="5" /></td>
			</tr></table>
			</div>
		</span>
	
	
	

		<span  class = "space">
			<p>7月30日 17:23</p>
			<font  color="red">凌晨的火车站里有一奇怪现象：女性乘客看起来会比想象中的更多。</font>

		</span>




		<span  class = "space">
			<p>7月7日 14:47</p>
			<font  color="red">调查数据一大优势是能够提供关于行为信念的直接证据，但也有四各方面的批判：样本量小且非代表性，精心设计的问题有时与模型所需的信息点不符，测量误差，个人行为有时是基于实际行动而非自我感知的。</font>

		</span>


		<span  class = "space">
			<p>7月7日 11:29</p>
			<font  color="red">这两位合作，值得细看</font>
			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->
			<table><tr>
			<td><img src="https://raw.githubusercontent.com/wuyy2007/resouce/master/webcontentpic/slhbf.png" height="100" width="70" margin="5" /></td>
			</tr></table>
			</div>
		</span>


		<span  class = "space">
			<p>7月6日 17:02</p>
			<font  color="red">某些复杂决策环境下，选择它并不是因为它是最好的，而是因别无可选</font>
			<div class="over"></div><!--背景层-->
			<div class="logoImg amplifyImg"><!--注意：此处的amlifyImg不可少-->
			<table><tr>
			<td><img src="https://raw.githubusercontent.com/wuyy2007/resouce/master/webcontentpic/ice_and_sunshine.jpg" height="103" width="200" margin="5" /></td>
			</tr></table>
			</div>
		</span>


		<span class = "space">

			<p>7月4日 21:15</p>
			<font  color="red">隔行听建议，本行靠自己。</font>

		</span>



		<span  class = "space">
			<p>6月21日 11:03</p>
			<font  color="red">总能看到人们对待自然灾害时的乐观心态--2019汉雨</font>

			<table><tr>

			<td>
				<video width="206" height="103" controls>
				  <source alt = "爱飙戏的" src="https://raw.githubusercontent.com/wuyy2007/resouce/master/webcontentpic/rainshow.mp4" type="video/mp4">
				  <source src="movie.ogg" type="video/ogg">
				  <source src="movie.webm" type="video/webm">
				您的浏览器不支持 video 标签。
				</video>			
			</td>
			</tr></table>

		</span>
	
