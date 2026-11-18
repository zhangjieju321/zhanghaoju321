

      -webkit-animation-timing-function: ease-in-out;
      animation-timing-function: ease-in-out;
      -webkit-animation-fill-mode: both;
      animation-fill-mode: both;
    }
    @keyframes superScaleIn{from{transform:scale(1.2);opacity:0}to{transform:scale(1);opacity:1}}

    .containerAnimate .mask{ position: absolute; width: 100%; height: 100%; left: 0; top: 0;background: #000;filter: alpha(opacity:50);opacity: 0.5; }
    .popWrap{ display: flex; align-items: center; justify-content: center; position: absolute; width: 100%; height: 100%; left: 0; top: 0; z-index: 1; }
    .popWrap .con{ position: relative; width: 300px; height: 300px;}
    .popWrap .close{ display: flex; align-items: flex-start; justify-content: center; position: absolute; z-index: 1; width: 50px; height: 50px; top: -4px; right: -50px;}
    .popWrap .link{ display: block; width: 100%; height: 100%;}
    .popWrap .link img{ width: 100%; height: 100%;}
    .containerAnimate.h5 .popWrap .con{ transform: scale(2); }
</style>
<div class="containerAnimate" id="zstAdPopup" style="display:none;">
    <div class="mask"></div>
    <div class="popWrap">
        <div class="con">
            <a href="javascript:;" class="close" onclick="document.querySelector('#zstAdPopup').style.display='none';">
                <svg t="1662540261941" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="17786" width="40" height="40"><path d="M571.733333 512l268.8-268.8c17.066667-17.066667 17.066667-42.666667 0-59.733333-17.066667-17.066667-42.666667-17.066667-59.733333 0L512 452.266667 243.2 183.466667c-17.066667-17.066667-42.666667-17.066667-59.733333 0-17.066667 17.066667-17.066667 42.666667 0 59.733333L452.266667 512 183.466667 780.8c-17.066667 17.066667-17.066667 42.666667 0 59.733333 8.533333 8.533333 19.2 12.8 29.866666 12.8s21.333333-4.266667 29.866667-12.8L512 571.733333l268.8 268.8c8.533333 8.533333 19.2 12.8 29.866667 12.8s21.333333-4.266667 29.866666-12.8c17.066667-17.066667 17.066667-42.666667 0-59.733333L571.733333 512z" p-id="17787" fill="#ffffff"></path></svg>
            </a>
            <a href="javascript:;" onclick="targetHref()" class="link">
                <img src="https://cdn.ttyingqiu.com/news/image/2023/5/17/202305171709000017.png">
            </a>
        </div>
    </div>
</div>


























<script>
	    $(document).ready(function(){
	    	zstOpenDataMask();
	    });
	
	    function zstOpenDataMask(){
	    	var openStatusName = null;
	    	if(location.pathname.indexOf('ssq')!=-1){
	    		openStatusName = "ttzs_zstAdPopupOpen_ssq";	
	    	}else if(location.pathname.indexOf('dlt')!=-1){
	    		openStatusName = "ttzs_zstAdPopupOpen_dlt";
	    	}
	    	if(!openStatusName){
	    		return;
	    	}
	        var openStatusVal = getCookie_zs(openStatusName);
	        if(openStatusVal==null || openStatusVal==''){
	            $("#zstAdPopup").attr("style","display:block;");
	            var ua=navigator.userAgent;
	       	 	if(!!ua.match(/AppleWebKit.*Mobile.*/)){
	       	 		$("#zstAdPopup").addClass("h5");	
	       	 	}
	            setCookie_zs(openStatusName,"opened",1);
	        }
	    }
	    function setCookie_zs(c_name,value,exDay)
	    {
	        var dayTime = new Date().getTime()+(60*60*24*exDay*1000);
	        var exdate = new Date(dayTime);
	        document.cookie=c_name+ "=" +escape(value)+";path=/;domain=.ttzoushi.com;expires="+exdate.toGMTString();
	    }
	    function getCookie_zs(c_name)
	    {
	        if (document.cookie.length>0)
	        {
	            c_start=document.cookie.indexOf(c_name + "=")
	            if (c_start!=-1)
	            {
	                c_start=c_start + c_name.length+1
	                c_end=document.cookie.indexOf(";",c_start)
	                if (c_end==-1) c_end=document.cookie.length
	                return unescape(document.cookie.substring(c_start,c_end))
	            }
	        }
	        return ""
	    }
	    function targetHref(){
	    	document.querySelector('#zstAdPopup').style.display='none';
	    	window.open("https://www.ttzoushi.com/page/web/downLoadYch.html")
	    }
	    
	</script>
<div class="conMain" style="margin-top:0;">
	<div class="conMain_top" style="z-index: 2">
		<div class="trend"> <a href="/dlt/" class="trend_ico dltLogo"></a>
			<span id="trend_pop">
				<p>大乐透图表走势</p>
				<a href="###" id="trend_xl" class="trend_xl"></a>
				<!--鼠标悬停-->
				<div id="trend_conList" class="trend_conList"> 
					 <em></em>
<ul>
    <li class="trend_conList_fc clearfix">
        <a href="/ssq/">双色球</a>
        <a href="/fc3d/">福彩3D</a>
        <a href="/hd15x5/">15选5</a>
        <a href="/qlc/">七乐彩</a>
        <a href="/df61/">东方6+1</a>
    </li>
    <li class="trend_conList_tc clearfix">
        <a href="/dlt/">大乐透</a>
        <a href="/qxc/">七星彩</a>
        <a href="/pl3/">排列3</a>
        <a href="/pl5/">排列5</a>
    </li>


</ul>
<script type="text/javascript" src="https://r.ttyingqiu.com/r/js/??zst/domain.js?v=20230717004"></script></div>
				<!--鼠标悬停-->
			</span>
		</div>
		<div class="conNav" style="width: 520px; left: 190px;">
			<ul class="clearfix">
				<li><strong><a href="/dlt/" id="hmzs_id">号码走势</a></strong></li>
				<li><strong><a href="/dlt/qqhmyl/" id="ylsj_id">遗漏数据</a></strong></li>
				<li><strong><a href="/dlt/openInfo/" id="lskj_id" class="conNav_active">历史开奖</a></strong></li>
				</ul>
		</div>
		<!--广告-->
		</div>
	<div class="conMain_bot" id="hmzs_top" style="display: none;">
		<ul class="clearfix">
			<li><a href="/dlt/">基本走势</a>|</li>
			<li><a href="/dlt/hqzs/">后区走势</a>|</li>
			<li><a href="/dlt/dwzs/">定位走势</a>|</li>
			<li><a href="/dlt/dxzs/">大小走势</a>|</li>
			<li><a href="/dlt/jozs/">奇偶走势</a>|</li>
			<li><a href="/dlt/zhzs/">质合走势</a>|</li>
			<li><a href="/dlt/c3ys/">除3余数</a>|</li>
			<li><a href="/dlt/5xzs/">五行走势</a>|</li>
			<li><a href="/dlt/hzzs/">和值走势</a>|</li>
			<li><a href="/dlt/kdzs/">跨度走势</a>|</li>
			<li><a href="/dlt/lhzs/">连号走势</a>|</li>
			<li><a href="/dlt/clg/">重邻孤</a>|</li>        
			<li><a href="/dlt/wszs/">尾数走势</a>|</li>
			<li><a href="/dlt/hlt/">行列图</a>|</li>
			<li><a href="/dlt/xjm/">新旧码</a>|</li>
			<li><a href="/dlt/lrfx/">冷热分析</a></li>
		</ul>
	</div>
	<div class="conMain_bot" id="ylsj_top" style="display: none;">
        <ul class="clearfix">
            <li><a href="/dlt/qqhmyl/">号码遗漏</a>|</li>
            <li><a href="/dlt/dxbiyl/">大小遗漏</a>|</li>
            <li><a href="/dlt/jobiyl/">奇偶遗漏</a>|</li>
            <li><a href="/dlt/zhbiyl/">质合遗漏</a>|</li>
            <li><a href="/dlt/c3ysyl/">除3余数遗漏</a>|</li>
            <li><a href="/dlt/5xyl/">五行遗漏</a>|</li>
            <li><a href="/dlt/hzyl/">和值遗漏</a>|</li>
            <li><a href="/dlt/lhgsyl/">连号遗漏</a>|</li>
            <li><a href="/dlt/kdyl/">跨度遗漏</a>|</li>
            <li><a href="/dlt/twsyl/">同尾数遗漏</a>|</li>
            <li><a href="/dlt/xjmyl/">新旧码遗漏</a>|</li>
            <li><a href="/dlt/clgyl/">重邻孤遗漏</a></li>
        </ul>
    </div>	
	<div class="conMain_bot" id="kxt_top" style="display: none;">
	    <ul class="clearfix">
	        <li><a href="/dlt/jhgs/">奇号个数</a>|</li>
	        <li><a href="/dlt/dhgs/">大号个数</a>|</li>
	        <li><a href="/dlt/zhgs/">质号个数</a>|</li>
	        <li><a href="/dlt/hmhz/">号码和值</a>|</li>
	        <li><a href="/dlt/wshz/">尾数和值</a>|</li>
	        <li><a href="/dlt/maxNum/">最大号</a>|</li>
	        <li><a href="/dlt/minNum/">最小号</a>|</li>
	        <li><a href="/dlt/lhjj/">邻号间距</a>|</li>
	        <li><a href="/dlt/wszus/">尾数组数</a>|</li>
	        <li><a href="/dlt/jhjj/">极号间距</a>|</li>
	        <li><a href="/dlt/jhlx/">奇号连续</a>|</li>
	        <li><a href="/dlt/ohlx/">偶号连续</a>|</li>
	        <li><a href="/dlt/lhgs/">连号个数</a>|</li>
	        <li><a href="/dlt/lhzus/">连号组数</a>|</li>
	        <li><a href="/dlt/acz/">AC值</a></li>
	    </ul>
	</div>
	<div class="conMain_bot" id="lskj_top" style="">
	    <ul class="clearfix">
	        <li><a href="/dlt/openInfo/">开奖信息</a>|</li>
	        <li><a href="/dlt/ballOrder/" class="conMain_bot_active">出球顺序</a>|</li>
	        <li><a href="/dlt/history/">历史同期</a>|</li>
	        <li><a href="/dlt/winPercent/">返奖比例</a></li>
	    </ul>
	</div>
</div>
<script type="text/javascript">
function init(){

		var url = window.location.href;
		if(url.indexOf("yl")!=-1){
			$("#ylsj_id").addClass("conNav_active");
			$("#ylsj_top").show();
		}else if(url.indexOf("/jhgs")!=-1||url.indexOf("/dhgs")!=-1||url.indexOf("/zhgs")!=-1||url.indexOf("/hmhz")!=-1
				||url.indexOf("/wshz")!=-1||url.indexOf("/maxNum")!=-1||url.indexOf("/minNum")!=-1||url.indexOf("/lhjj")!=-1
				||url.indexOf("/wszus")!=-1||url.indexOf("/jhjj")!=-1||url.indexOf("/jhlx")!=-1||url.indexOf("/ohlx")!=-1
				||url.indexOf("/lhgs")!=-1||url.indexOf("/lhzus")!=-1||url.indexOf("/acz")!=-1){
			$("#kxt_id").addClass("conNav_active");
			$("#kxt_top").show();
		}else if(url.indexOf("history")>-1||url.indexOf("openInfo")>-1||url.indexOf("ballOrder")>-1||url.indexOf("winPercent")>-1){
			$("#lskj_id").addClass("conNav_active");
			$("#lskj_top").show();
		}else if(url.indexOf("betTrend")>-1){
			$("#tzqx_id").addClass("conNav_active");
		}else{
			$("#hmzs_id").addClass("conNav_active");
			$("#hmzs_top").show();
		}
	}
	init();
</script><form action="/dlt/ballOrder/" method="post" name="form1">
    <div class="periods">
        <p class="remnant">
            <strong>大乐透:</strong>出球顺序
        </p>
        <div class="selectPeriods" id="selectdiv" style="right: 350px;">
	<span>显示期数</span>
	<span>
		<select class="periodsList" id="select_id" onchange="sizeSelect();return false;">
			<option value="30">最近30期</option>
			<option value="50">最近50期</option>
			<option value="100" selected="selected">最近100期</option>
			<option value="10">最近10期</option>
			<option value="">自定义期数</option>
		</select>
	</span>
</div>

<div class="selectPeriods" style="right:370px; width: 230px; display:none;" id="input_id">
	<span>
		<input type="text" id="start_id" name="startIssue" onkeyup="value=this.value.replace(/\D+/g,'')" oncontextmenu="return false;" onpaste="return false;" value="" style="width:50px;border: 1px solid #BAE2F9">期至
		<input type="text" id="end_id" name="endIssue" onkeyup="value=this.value.replace(/\D+/g,'')" oncontextmenu="return false;" onpaste="return false;" value="" style="width:50px;border: 1px solid #BAE2F9">期<a onclick="showSelect();return false;">返回</a>
	</span>
	<a href="javascript:void(0);" class="checkBtn" onclick="searchRes();return false;">查询</a>
</div>

<div class="kjHistory" style="right:100px;">
	<span>开奖:</span>
	<a style="text-decoration: none;" href="javascript:void(0);" onclick="putValue('1');return false;">一</a>
	<a style="text-decoration: none;" href="javascript:void(0);" onclick="putValue('3');return false;">三</a>
	<a style="text-decoration: none;" href="javascript:void(0);" onclick="putValue('6');return false;">六</a>
	<a style="text-decoration: none;" href="javascript:void(0);" class="date_active" onclick="putValue('');return false;">全</a>
	<span class="HistorySelect">历史第</span>
	<a href="javascript:void(0);" id="preIsue_id" onclick="putValue('093');return false;">093</a>
	<a href="javascript:void(0);" id="current_id" onclick="putValue('094');return false;">094</a>
<span>期</span>
<input type="hidden" id="openDate_id" value="">
</div>
<script type="text/javascript">
var start = "";
if(start==""){
	jQuery("#selectdiv").show();
	jQuery("#input_id").hide();
}else{
	jQuery("#selectdiv").hide();
	jQuery("#input_id").show();
}
var last= $("#preIsue_id").html();
var cur = $("#current_id").html();
var openDate = $("#openDate_id").val();
if(openDate==cur){
	$("#current_id").addClass("date_active");
}else if(openDate==last){
	$("#preIsue_id").addClass("date_active");
}
</script></div>

    <div class="mainTab">
        <table class="fzTab nbt">
            <tbody>
              <tr class="h20">
                <th rowspan="2" class="w75 th_hover">
                 <a href="javascript:void(0);" onclick="sort();return false;">期号
                      <span class="up"></span></a>	                
                </th>
                <th rowspan="2" class="w75">开奖日期</th>
                <th colspan="5" class="w75 ">出球顺序</th>
                <th colspan="7">开奖号码（按大小排列）</th>
              </tr>
              <tr class="h20">
                <th class="b_white">1</th>
                <th class="b_white">2</th>
                <th class="b_white">3</th>
                <th class="b_white">4</th>
                <th class="b_white">5</th>
                <th colspan="5" class="b_white">红球号码</th>
                <th colspan="2" class="b_white">蓝球号码</th>
              </tr>
              
               <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23093</td>
	                  <td>2023-08-14</td>
	                  <td class="redColor" style="font-weight:bold">19</td>
	                  <td class="redColor" style="font-weight:bold">17</td>
	                  <td class="redColor" style="font-weight:bold">21</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td class="redColor" style="font-weight:bold">14</td>
	                  <td>11</td>
	                  <td>14</td>
	                  <td>17</td>
	                  <td>19</td>
	                  <td>21</td>
	                  <td class="blueColor">01</td>
	                  <td class="blueColor">05</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23092</td>
	                  <td>2023-08-12</td>
	                  <td class="redColor" style="font-weight:bold">16</td>
	                  <td class="redColor" style="font-weight:bold">21</td>
	                  <td class="redColor" style="font-weight:bold">03</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td>03</td>
	                  <td>16</td>
	                  <td>21</td>
	                  <td>26</td>
	                  <td>32</td>
	                  <td class="blueColor">03</td>
	                  <td class="blueColor">12</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23091</td>
	                  <td>2023-08-09</td>
	                  <td class="redColor" style="font-weight:bold">29</td>
	                  <td class="redColor" style="font-weight:bold">16</td>
	                  <td class="redColor" style="font-weight:bold">18</td>
	                  <td class="redColor" style="font-weight:bold">28</td>
	                  <td class="redColor" style="font-weight:bold">06</td>
	                  <td>06</td>
	                  <td>16</td>
	                  <td>18</td>
	                  <td>28</td>
	                  <td>29</td>
	                  <td class="blueColor">07</td>
	                  <td class="blueColor">11</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23090</td>
	                  <td>2023-08-07</td>
	                  <td class="redColor" style="font-weight:bold">19</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td class="redColor" style="font-weight:bold">12</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td>08</td>
	                  <td>11</td>
	                  <td>12</td>
	                  <td>19</td>
	                  <td>35</td>
	                  <td class="blueColor">11</td>
	                  <td class="blueColor">12</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23089</td>
	                  <td>2023-08-05</td>
	                  <td class="redColor" style="font-weight:bold">20</td>
	                  <td class="redColor" style="font-weight:bold">12</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td class="redColor" style="font-weight:bold">03</td>
	                  <td>03</td>
	                  <td>12</td>
	                  <td>20</td>
	                  <td>26</td>
	                  <td>35</td>
	                  <td class="blueColor">02</td>
	                  <td class="blueColor">12</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23088</td>
	                  <td>2023-08-02</td>
	                  <td class="redColor" style="font-weight:bold">22</td>
	                  <td class="redColor" style="font-weight:bold">14</td>
	                  <td class="redColor" style="font-weight:bold">24</td>
	                  <td class="redColor" style="font-weight:bold">16</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td>08</td>
	                  <td>14</td>
	                  <td>16</td>
	                  <td>22</td>
	                  <td>24</td>
	                  <td class="blueColor">09</td>
	                  <td class="blueColor">12</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23087</td>
	                  <td>2023-07-31</td>
	                  <td class="redColor" style="font-weight:bold">19</td>
	                  <td class="redColor" style="font-weight:bold">16</td>
	                  <td class="redColor" style="font-weight:bold">04</td>
	                  <td class="redColor" style="font-weight:bold">24</td>
	                  <td class="redColor" style="font-weight:bold">03</td>
	                  <td>03</td>
	                  <td>04</td>
	                  <td>16</td>
	                  <td>19</td>
	                  <td>24</td>
	                  <td class="blueColor">04</td>
	                  <td class="blueColor">05</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23086</td>
	                  <td>2023-07-29</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td class="redColor" style="font-weight:bold">20</td>
	                  <td class="redColor" style="font-weight:bold">03</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td class="redColor" style="font-weight:bold">15</td>
	                  <td>03</td>
	                  <td>11</td>
	                  <td>15</td>
	                  <td>20</td>
	                  <td>35</td>
	                  <td class="blueColor">07</td>
	                  <td class="blueColor">11</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23085</td>
	                  <td>2023-07-26</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td class="redColor" style="font-weight:bold">31</td>
	                  <td class="redColor" style="font-weight:bold">12</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td>11</td>
	                  <td>12</td>
	                  <td>26</td>
	                  <td>31</td>
	                  <td>35</td>
	                  <td class="blueColor">05</td>
	                  <td class="blueColor">07</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23084</td>
	                  <td>2023-07-24</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td class="redColor" style="font-weight:bold">03</td>
	                  <td class="redColor" style="font-weight:bold">24</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td class="redColor" style="font-weight:bold">05</td>
	                  <td>03</td>
	                  <td>05</td>
	                  <td>08</td>
	                  <td>24</td>
	                  <td>32</td>
	                  <td class="blueColor">07</td>
	                  <td class="blueColor">08</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23083</td>
	                  <td>2023-07-22</td>
	                  <td class="redColor" style="font-weight:bold">21</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td class="redColor" style="font-weight:bold">15</td>
	                  <td class="redColor" style="font-weight:bold">13</td>
	                  <td class="redColor" style="font-weight:bold">25</td>
	                  <td>13</td>
	                  <td>15</td>
	                  <td>21</td>
	                  <td>25</td>
	                  <td>32</td>
	                  <td class="blueColor">09</td>
	                  <td class="blueColor">10</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23082</td>
	                  <td>2023-07-19</td>
	                  <td class="redColor" style="font-weight:bold">02</td>
	                  <td class="redColor" style="font-weight:bold">09</td>
	                  <td class="redColor" style="font-weight:bold">20</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td class="redColor" style="font-weight:bold">15</td>
	                  <td>02</td>
	                  <td>08</td>
	                  <td>09</td>
	                  <td>15</td>
	                  <td>20</td>
	                  <td class="blueColor">03</td>
	                  <td class="blueColor">09</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23081</td>
	                  <td>2023-07-17</td>
	                  <td class="redColor" style="font-weight:bold">28</td>
	                  <td class="redColor" style="font-weight:bold">05</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td class="redColor" style="font-weight:bold">23</td>
	                  <td class="redColor" style="font-weight:bold">06</td>
	                  <td>05</td>
	                  <td>06</td>
	                  <td>23</td>
	                  <td>28</td>
	                  <td>35</td>
	                  <td class="blueColor">07</td>
	                  <td class="blueColor">10</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23080</td>
	                  <td>2023-07-15</td>
	                  <td class="redColor" style="font-weight:bold">16</td>
	                  <td class="redColor" style="font-weight:bold">01</td>
	                  <td class="redColor" style="font-weight:bold">09</td>
	                  <td class="redColor" style="font-weight:bold">02</td>
	                  <td class="redColor" style="font-weight:bold">30</td>
	                  <td>01</td>
	                  <td>02</td>
	                  <td>09</td>
	                  <td>16</td>
	                  <td>30</td>
	                  <td class="blueColor">01</td>
	                  <td class="blueColor">11</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23079</td>
	                  <td>2023-07-12</td>
	                  <td class="redColor" style="font-weight:bold">34</td>
	                  <td class="redColor" style="font-weight:bold">06</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">29</td>
	                  <td>06</td>
	                  <td>08</td>
	                  <td>26</td>
	                  <td>29</td>
	                  <td>34</td>
	                  <td class="blueColor">05</td>
	                  <td class="blueColor">08</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23078</td>
	                  <td>2023-07-10</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">03</td>
	                  <td class="redColor" style="font-weight:bold">06</td>
	                  <td class="redColor" style="font-weight:bold">02</td>
	                  <td class="redColor" style="font-weight:bold">27</td>
	                  <td>02</td>
	                  <td>03</td>
	                  <td>06</td>
	                  <td>26</td>
	                  <td>27</td>
	                  <td class="blueColor">07</td>
	                  <td class="blueColor">08</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23077</td>
	                  <td>2023-07-08</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">18</td>
	                  <td class="redColor" style="font-weight:bold">05</td>
	                  <td class="redColor" style="font-weight:bold">16</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td>05</td>
	                  <td>16</td>
	                  <td>18</td>
	                  <td>26</td>
	                  <td>35</td>
	                  <td class="blueColor">03</td>
	                  <td class="blueColor">06</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23076</td>
	                  <td>2023-07-05</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td class="redColor" style="font-weight:bold">34</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td class="redColor" style="font-weight:bold">09</td>
	                  <td>08</td>
	                  <td>09</td>
	                  <td>11</td>
	                  <td>26</td>
	                  <td>34</td>
	                  <td class="blueColor">02</td>
	                  <td class="blueColor">07</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23075</td>
	                  <td>2023-07-03</td>
	                  <td class="redColor" style="font-weight:bold">23</td>
	                  <td class="redColor" style="font-weight:bold">07</td>
	                  <td class="redColor" style="font-weight:bold">17</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td class="redColor" style="font-weight:bold">20</td>
	                  <td>07</td>
	                  <td>17</td>
	                  <td>20</td>
	                  <td>23</td>
	                  <td>32</td>
	                  <td class="blueColor">05</td>
	                  <td class="blueColor">11</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23074</td>
	                  <td>2023-07-01</td>
	                  <td class="redColor" style="font-weight:bold">22</td>
	                  <td class="redColor" style="font-weight:bold">13</td>
	                  <td class="redColor" style="font-weight:bold">03</td>
	                  <td class="redColor" style="font-weight:bold">29</td>
	                  <td class="redColor" style="font-weight:bold">34</td>
	                  <td>03</td>
	                  <td>13</td>
	                  <td>22</td>
	                  <td>29</td>
	                  <td>34</td>
	                  <td class="blueColor">02</td>
	                  <td class="blueColor">09</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23073</td>
	                  <td>2023-06-28</td>
	                  <td class="redColor" style="font-weight:bold">30</td>
	                  <td class="redColor" style="font-weight:bold">25</td>
	                  <td class="redColor" style="font-weight:bold">28</td>
	                  <td class="redColor" style="font-weight:bold">15</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td>15</td>
	                  <td>25</td>
	                  <td>28</td>
	                  <td>30</td>
	                  <td>35</td>
	                  <td class="blueColor">08</td>
	                  <td class="blueColor">10</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23072</td>
	                  <td>2023-06-26</td>
	                  <td class="redColor" style="font-weight:bold">06</td>
	                  <td class="redColor" style="font-weight:bold">09</td>
	                  <td class="redColor" style="font-weight:bold">14</td>
	                  <td class="redColor" style="font-weight:bold">05</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td>05</td>
	                  <td>06</td>
	                  <td>09</td>
	                  <td>11</td>
	                  <td>14</td>
	                  <td class="blueColor">02</td>
	                  <td class="blueColor">04</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23071</td>
	                  <td>2023-06-24</td>
	                  <td class="redColor" style="font-weight:bold">34</td>
	                  <td class="redColor" style="font-weight:bold">02</td>
	                  <td class="redColor" style="font-weight:bold">12</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td>02</td>
	                  <td>11</td>
	                  <td>12</td>
	                  <td>32</td>
	                  <td>34</td>
	                  <td class="blueColor">10</td>
	                  <td class="blueColor">12</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'" style="background: rgb(239, 243, 247);">
	                  <td>23070</td>
	                  <td>2023-06-21</td>
	                  <td class="redColor" style="font-weight:bold">29</td>
	                  <td class="redColor" style="font-weight:bold">33</td>
	                  <td class="redColor" style="font-weight:bold">10</td>
	                  <td class="redColor" style="font-weight:bold">26</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td>10</td>
	                  <td>26</td>
	                  <td>29</td>
	                  <td>32</td>
	                  <td>33</td>
	                  <td class="blueColor">03</td>
	                  <td class="blueColor">11</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''" style="">
	                  <td>23069</td>
	                  <td>2023-06-19</td>
	                  <td class="redColor" style="font-weight:bold">25</td>
	                  <td class="redColor" style="font-weight:bold">20</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td class="redColor" style="font-weight:bold">21</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td>08</td>
	                  <td>20</td>
	                  <td>21</td>
	                  <td>25</td>
	                  <td>32</td>
	                  <td class="blueColor">05</td>
	                  <td class="blueColor">07</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'">
	                  <td>23068</td>
	                  <td>2023-06-17</td>
	                  <td class="redColor" style="font-weight:bold">21</td>
	                  <td class="redColor" style="font-weight:bold">24</td>
	                  <td class="redColor" style="font-weight:bold">27</td>
	                  <td class="redColor" style="font-weight:bold">31</td>
	                  <td class="redColor" style="font-weight:bold">22</td>
	                  <td>21</td>
	                  <td>22</td>
	                  <td>24</td>
	                  <td>27</td>
	                  <td>31</td>
	                  <td class="blueColor">07</td>
	                  <td class="blueColor">08</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''">
	                  <td>23067</td>
	                  <td>2023-06-14</td>
	                  <td class="redColor" style="font-weight:bold">33</td>
	                  <td class="redColor" style="font-weight:bold">28</td>
	                  <td class="redColor" style="font-weight:bold">35</td>
	                  <td class="redColor" style="font-weight:bold">02</td>
	                  <td class="redColor" style="font-weight:bold">30</td>
	                  <td>02</td>
	                  <td>28</td>
	                  <td>30</td>
	                  <td>33</td>
	                  <td>35</td>
	                  <td class="blueColor">02</td>
	                  <td class="blueColor">10</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'">
	                  <td>23066</td>
	                  <td>2023-06-12</td>
	                  <td class="redColor" style="font-weight:bold">06</td>
	                  <td class="redColor" style="font-weight:bold">13</td>
	                  <td class="redColor" style="font-weight:bold">11</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td class="redColor" style="font-weight:bold">30</td>
	                  <td>06</td>
	                  <td>11</td>
	                  <td>13</td>
	                  <td>30</td>
	                  <td>32</td>
	                  <td class="blueColor">01</td>
	                  <td class="blueColor">03</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" onmouseout="this.style.background=''">
	                  <td>23065</td>
	                  <td>2023-06-10</td>
	                  <td class="redColor" style="font-weight:bold">21</td>
	                  <td class="redColor" style="font-weight:bold">16</td>
	                  <td class="redColor" style="font-weight:bold">25</td>
	                  <td class="redColor" style="font-weight:bold">08</td>
	                  <td class="redColor" style="font-weight:bold">14</td>
	                  <td>08</td>
	                  <td>14</td>
	                  <td>16</td>
	                  <td>21</td>
	                  <td>25</td>
	                  <td class="blueColor">03</td>
	                  <td class="blueColor">12</td>
	                  </tr>
              <tr onmouseover="this.style.background='#fff7d8'" class="camBlue" onmouseout="this.style.background='#eff3f7'">
	                  <td>23064</td>
	                  <td>2023-06-07</td>
	                  <td class="redColor" style="font-weight:bold">32</td>
	                  <td class="redColor" style="font-weight:bold">09</td>
	                  <td class="redColor" style="font-weight:bold">02</td>
	                  <td class="redColor" style="font-weight:bold">06</td>
	                  <td class="redColor" style="font-weight:bold">31</td>
	                  <td>02</td>
	                  <td>06</td>
	                  <td>09</td>
	                  <td>31</td>
	                  <td>32</td>
	                  <td class="blueColor">03</td>
	                  <td class="blueColor">07</td>
	                  </tr>
              </tbody>
    </table>
    </div>
    <!--分页-->
    <div class="page">
	       &nbsp; 每页显示  <select id="jq_rank_pages_select" onchange="dotiaoshu();">
                             <option value="30">30</option>
          			</select>&nbsp; 条
          			<ul class="pageList clearfix"><li><a class="disabled">&lt;上一页</a></li><li><a class="active">1</a></li><li><a id="jq_rank_pager_tohref_2" href="javascript:getPage(2);">2</a></li><li><a id="jq_rank_pager_tohref_3" href="javascript:getPage(3);">3</a></li><li><a id="jq_rank_pager_tohref_4" href="javascript:getPage(4);">4</a></li><li><a id="jq_rank_pager_tohref_2" href="javascript:getPage(2);">下一页&gt;</a></li> </ul><p class="page_skip">第<input onkeyup="check(this)" id="jq_rank_pages_to_numbers_text" value="1" class="jq_input_shadow shadow_input" type="text" size="1">页
              	<a onclick="page_xz();return false;" href="javascript:void(0);" class="checkBtn">跳转</a></p>
     </div>
    <!--分页-->
   		 <input type="hidden" id="size_id" name="maxsize" value="100">
         <input type="hidden" id="sort_id" name="sortTag" value="down">
         <input type="hidden" id="date_id" name="openDate" value="">
         <input type="hidden" id="currentPage_id" name="currentPage" value="1">
         <input type="hidden" id="pageSize_id" name="pageSize" value="30">
         <input type="hidden" id="gameIndex_id" name="gameIndex" value="201">
         <input type="hidden" id="pageInfo_id" name="pageInfo" value="ballOrder">
      </form>
</div>
<div class="floatDLT" style="display: none">
	<div id="data_id"></div>
	<div class="haomaCell">
    	<dl class="redNum">
        	<dt>号码区</dt>
            <dd id="red_01"><a href="javascript:void(0);">01</a>
            	<div style="left: 0px; display: none;" class="absDltTips">
                	<i style="left: -2px;" class="absJ_a"><i class="absJ_b"></i></i>
                    <p>1.最近50期内同出码:<strong class="red" id="no1"></strong>(<span id="smae1"></span>次)
                    			<strong class="red" id="no2"></strong>(<span id="smae2"></span>次)
                    			<strong class="red" id="no3"></strong>(<span id="smae3"></span>次)</p>
                    <p>2.当前期该号码被本站会员投注<strong id="betId"></strong>次</p>
                    <p>3.该号码历史上总共出现<strong id="allTimes"></strong>次，今年出现<strong id="yearTimes"></strong>次</p>
                </div>
            </dd>
            <script type="text/javascript">
        		for ( var i = 2; i <= 35; i++) {
					var i = i<10 ? "0"+i : i;
					document.write('<dd id="red_' + i + '"><a href="javascript:void(0);">' + i + '</a></dd>');
				}
        	</script><dd id="red_02"><a href="javascript:void(0);">02</a></dd><dd id="red_03"><a href="javascript:void(0);">03</a></dd><dd id="red_04"><a href="javascript:void(0);">04</a></dd><dd id="red_05"><a href="javascript:void(0);">05</a></dd><dd id="red_06"><a href="javascript:void(0);">06</a></dd><dd id="red_07"><a href="javascript:void(0);">07</a></dd><dd id="red_08"><a href="javascript:void(0);">08</a></dd><dd id="red_09"><a href="javascript:void(0);">09</a></dd><dd id="red_10"><a href="javascript:void(0);">10</a></dd><dd id="red_11"><a href="javascript:void(0);">11</a></dd><dd id="red_12"><a href="javascript:void(0);">12</a></dd><dd id="red_13"><a href="javascript:void(0);">13</a></dd><dd id="red_14"><a href="javascript:void(0);">14</a></dd><dd id="red_15"><a href="javascript:void(0);">15</a></dd><dd id="red_16"><a href="javascript:void(0);">16</a></dd><dd id="red_17"><a href="javascript:void(0);">17</a></dd><dd id="red_18"><a href="javascript:void(0);">18</a></dd><dd id="red_19"><a href="javascript:void(0);">19</a></dd><dd id="red_20"><a href="javascript:void(0);">20</a></dd><dd id="red_21"><a href="javascript:void(0);">21</a></dd><dd id="red_22"><a href="javascript:void(0);">22</a></dd><dd id="red_23"><a href="javascript:void(0);">23</a></dd><dd id="red_24"><a href="javascript:void(0);">24</a></dd><dd id="red_25"><a href="javascript:void(0);">25</a></dd><dd id="red_26"><a href="javascript:void(0);">26</a></dd><dd id="red_27"><a href="javascript:void(0);">27</a></dd><dd id="red_28"><a href="javascript:void(0);">28</a></dd><dd id="red_29"><a href="javascript:void(0);">29</a></dd><dd id="red_30"><a href="javascript:void(0);">30</a></dd><dd id="red_31"><a href="javascript:void(0);">31</a></dd><dd id="red_32"><a href="javascript:void(0);">32</a></dd><dd id="red_33"><a href="javascript:void(0);">33</a></dd><dd id="red_34"><a href="javascript:void(0);">34</a></dd><dd id="red_35"><a href="javascript:void(0);">35</a></dd>
        </dl>
        <dl class="blueNum">
        	<script type="text/javascript">
        		for ( var i = 1; i <= 12; i++) {
					var i = i<10 ? "0"+i : i;
					document.write('<dd id="blue_' + i + '"><a href="javascript:void(0);">' + i + '</a></dd>');
				}
        	</script><dd id="blue_01"><a href="javascript:void(0);">01</a></dd><dd id="blue_02"><a href="javascript:void(0);">02</a></dd><dd id="blue_03"><a href="javascript:void(0);">03</a></dd><dd id="blue_04"><a href="javascript:void(0);">04</a></dd><dd id="blue_05"><a href="javascript:void(0);">05</a></dd><dd id="blue_06"><a href="javascript:void(0);">06</a></dd><dd id="blue_07"><a href="javascript:void(0);">07</a></dd><dd id="blue_08"><a href="javascript:void(0);">08</a></dd><dd id="blue_09"><a href="javascript:void(0);">09</a></dd><dd id="blue_10"><a href="javascript:void(0);">10</a></dd><dd id="blue_11"><a href="javascript:void(0);">11</a></dd><dd id="blue_12"><a href="javascript:void(0);">12</a></dd>
        </dl>
    </div>
	<div class="ball_center">
        <div class="redball_qu">
            <h5>前区号码</h5>
            <div class="ball_box">
                <div class="red_hang">
                    <ul>
                    	<script type="text/javascript">
			        		for ( var i = 1; i <= 35; i++) {
								var i = i<10 ? "0"+i : i;
								document.write('<li>' + i + '</li>');
							}
			        	</script><li>01</li><li>02</li><li>03</li><li>04</li><li>05</li><li>06</li><li>07</li><li>08</li><li>09</li><li>10</li><li>11</li><li>12</li><li>13</li><li>14</li><li>15</li><li>16</li><li>17</li><li>18</li><li>19</li><li>20</li><li>21</li><li>22</li><li>23</li><li>24</li><li>25</li><li>26</li><li>27</li><li>28</li><li>29</li><li>30</li><li>31</li><li>32</li><li>33</li><li>34</li><li>35</li>
                     </ul>
                 </div>                   
                <div class="clear" id="redList"></div>
            </div>
            
        </div>
        <div class="blueball_qu">
            <h5>后区号码</h5>
            <div class="ball_box">
              <div class="blue_hang">
                <ul>
					<script type="text/javascript">
						for ( var i = 1; i <= 12; i++) {
							var i = i<10 ? "0"+i : i;
							document.write('<li>' + i + '</li>');
						}
					</script><li>01</li><li>02</li><li>03</li><li>04</li><li>05</li><li>06</li><li>07</li><li>08</li><li>09</li><li>10</li><li>11</li><li>12</li>
                </ul>
                </div>
                <div class="clear" id="blueList"></div>
            </div>            
        </div>
        <div class="tuzhuCell">
        	<a href="javascript:void(0);" class="addToBox">添加到选号篮</a>
            <div class="selectInfo">您选择了<strong class="blue" id="count_id">0</strong>注号码，投注金额为<strong class="red" id="money_id">0</strong>元</div>
            <!--广告-->
            <div class="btnBox"><a href="javascript:void(0);" class="goHaomaBox">选号篮(<span id="count">0</span>)注</a></div>
        </div>
        <div class="clear"></div>        
    </div>
</div>
<div class="hidden_count" style="display: none;">0</div>
<div class="hidden_money" style="display: none;">0</div>
<div class="hidden_list" style="display: none;"></div>
<script type="text/javascript" src="/static/no_cache/codetrait/data/ballInfo_201.js"></script>

	<script type="text/javascript" src="https://r.ttyingqiu.com/r/js/??zst/analysis/dlt/numAreaTips.js,
common/webdialog/webDialog.js?v=20230717004"></script>
<link href="https://r.ttyingqiu.com/r/css/??common/webdialog/new2010-min.css?v=20230717004" type="text/css" rel="stylesheet">

</div>
<div class="footer mt30">
	<div class="wrap1200 clearfix">
		<div class="footNav fl clearfix">
			<dl>
				<dt>数据服务</dt>
				<dd><a href="https://kaijiang.ttzoushi.com">开奖公告</a></dd>
				<dd><a href="https://zst.ttzoushi.com">走势图</a></dd>
				<dd><a href="https://www.ttzoushi.com/information/home">资讯</a></dd>
			</dl>
			<dl>
				<dt>分析预测</dt>
				<dd><a href="https://www.ttzoushi.com/lottery/index">专家推荐</a></dd>
				<!-- 
				<dd><a href="javascript:;">工具箱</a></dd> -->
			</dl>
			<dl>
				<dt>服务与支持</dt>
				<dd><a href="javascript:;" onclick="window.open('https://www.ttzoushi.com/page/web/downLoadYch.html')">下载天天走势</a></dd>
				<!-- <dd><a href="javascript:;">关注天天走势公众号</a></dd> -->
				<dd><a href="https://www.ttzoushi.com/home/digit-help">帮助中心</a></dd>
			</dl>
		</div>
		<div class="footRight fr">
			<ul>
				<li>
					<div class="contactInfo">
						<div class="phone">
							<div class="phoneIcon">
								<svg t="1645694670871" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="35836" width="20" height="20"><path d="M618.3 756.9l37.9-71.2c11.2-21 35.3-31.7 58.4-26L888 702.9c23.1 5.8 39.4 26.6 39.4 50.4l0.1 72.6h0.5v50.2c0 29.7-24.9 53.9-54.6 52-415.9-27-748.4-359.5-775.3-775.3-1.9-29.7 22.2-54.6 52-54.6h50.2v0.2l71.1 0.1c23.9 0 44.7 16.3 50.4 39.4L365 311.3c5.8 23.1-4.9 47.3-26 58.5L268.9 407c72.3 153.7 195.8 277.4 349.4 349.9z" p-id="35837" fill="#ffffff"></path></svg>
							</div>
							<div class="txt">
								<h6 id="kfTxt_phone">(0755) 61619788</h6>
								<p>服务时间09:00-18:00</p>
							</div>
						</div>
						<div class="butler">
							<a href="javascript:;">微信联系管家</a>
							<div class="butlerEwm" id="kfTxt_qrcode">
								<img src="https://cdn.ttyingqiu.com/news/image/2021/4/22/202104221134000027.jpg">
								<p>如有疑问<br>请添加管家微信咨询</p>
							</div>
						</div>
					</div>
				</li>
				<li>
					<img src="https://r.ttyingqiu.com/r/images/common/ttzs/download/ttzs_dl_5301.png">
					<p>天天走势App</p>
				</li>
				<li>
					<img src="https://r.ttyingqiu.com/r/images/common/ttzs/ttzsgzh.jpg">
					<p>天天走势公众号</p>
				</li>
			</ul>
		</div>	
	</div>
	<div class="copyRightWrap">
		<div class="wrap1200">
			<div class="copyRight">
				<span>Copyright © 2022 天天走势版权所有</span>   
				<span class="ml10">南京盈体信息科技有限公司</span>   
					<span class="ml10 mr30"><a href="https://beian.miit.gov.cn/#/Integrated/index" target="_blank" style="color: rgba(255,255,255,.5);">ICP证：苏ICP备19035387号-4</a></span>   					
				</div>
		</div>
	</div>
</div>

<!--右下角悬浮菜单-->
<div class="goFixedNew">
    <a href="javascript:;" class="downA jq_downBtn">
        <i>
            <svg t="1616482845223" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="15494" width="16" height="16"><path d="M813.176471 0H210.823529a60.235294 60.235294 0 0 0-60.235294 60.235294v903.529412a60.235294 60.235294 0 0 0 60.235294 60.235294h602.352942a60.235294 60.235294 0 0 0 60.235294-60.235294V60.235294a60.235294 60.235294 0 0 0-60.235294-60.235294z m0 963.764706H210.823529v-194.861177h602.352942zM210.823529 708.668235V60.235294h602.352942v648.432941z" fill="#ffffff" p-id="15495"></path><path d="M451.764706 899.614118h120.470588a30.117647 30.117647 0 0 0 0-60.235294h-120.470588a30.117647 30.117647 0 0 0 0 60.235294z" fill="#ffffff" p-id="15496"></path></svg>
        </i>
        <span>下载</span>
    </a>
    <div class="fixedEwm jq_fixedEwm" style="bottom:53px;height:190px">
        <div class="tit">下载手机客户端</div>
        <ul>
            <li>
                <img src="https://r.ttyingqiu.com/r/images/common/ttzs/download/ttzs_dl_5301.png">
                <h5>天天走势App</h5>
                <p>好用的彩票走势图</p>
            </li>
        </ul>
    </div>
    <a href="javascript:;" class="kf jq_kf">
        <i>
            <svg t="1616482973981" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="19847" width="16" height="16"><path d="M365.006 485.574c0 39.639 33.033 72.671 72.671 72.671 39.64 0 72.671-33.032 72.671-72.67 0-39.64-33.032-72.672-72.67-72.672-41.29 0-72.672 33.032-72.672 72.671z m325.368-72.67c-39.639 0-72.67 33.031-72.67 72.67s33.031 72.671 72.67 72.671 72.671-33.032 72.671-72.67c0-39.64-33.032-72.672-72.67-72.672z m279.123 14.864h-4.955C914.994 256 759.742 178.374 693.677 146.994c-3.303-1.652-4.954-3.304-8.258-4.955 8.258-8.258 18.168-19.82 21.471-34.684 3.304-16.516-1.651-33.032-13.213-44.594-9.91-11.561-31.38-34.684-158.554-18.167C411.252 57.806 118.916 156.904 61.11 427.768h-6.607c-21.47 0-37.987 16.516-37.987 37.987v120.568c0 21.47 16.516 37.987 37.987 37.987h6.607c42.942 211.406 221.316 303.896 393.084 322.064v1.652c0 21.47 16.516 37.987 37.987 37.987h155.251c21.471 0 37.987-16.516 37.987-37.987v-90.839c0-21.47-16.516-37.987-37.987-37.987H492.181c-21.471 0-37.987 16.516-37.987 37.987v4.955c-99.097-11.561-265.91-61.11-310.504-242.787 11.562-6.607 21.471-19.82 21.471-34.684V464.103c0-14.864-8.258-26.426-19.82-33.032 66.065-257.652 396.388-305.548 399.691-307.2 21.471-3.303 37.987-3.303 52.852-4.955-3.303 8.258-4.955 16.516-4.955 26.426 0 13.213 4.955 33.032 26.426 51.2 8.258 8.258 19.82 13.213 39.639 23.123C716.8 247.742 835.716 307.2 880.31 431.07c-11.562 6.606-19.82 18.168-19.82 33.032v120.568c0 21.47 16.516 37.987 37.987 37.987h72.671c21.471 0 37.987-16.516 37.987-37.987V464.103c-1.651-19.82-18.167-36.335-39.638-36.335z" p-id="19848" fill="#ffffff"></path></svg>
        </i>
        <span>客服</span>
        
        <div class="kfWrap">
	        <div class="kfTxt">
	            <div class="ewm clearfix">
	                <img src="https://cdn.ttyingqiu.com/news/image/2021/4/22/202104221134000027.jpg">
	                <div class="txt">
	                    <h5 class="fs16 c333">有问题找管家</h5>
	                    <p class="fs12 c999">微信扫码加管家</p>
	                </div>
	            </div>
	            <div class="phoneInfo">
	            	<h5 class="fs14 c333" id="kf_phone">客服电话：(0755) 61619788</h5>
	            	<p class="fs12 c999">服务时间  09:00~18:00</p>
	            </div>
	        </div>
	    </div>
    </a>
    
    <a href="javascript:;" class="kffk jq_kffk" onclick="goFeedBack()">
        <i>
            <svg t="1616483050339" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="24665" width="16" height="16"><path d="M815.74 412.26c29.72-29.71 46.09-69.22 46.09-111.25s-16.37-81.55-46.09-111.25L712.25 86.26C682.54 56.56 643.02 40.19 601 40.19s-81.55 16.37-111.25 46.08L117.42 458.6 85.11 816.91l358.33-32.32 372.3-372.33zM546.35 142.87c30.13-30.13 79.17-30.13 109.3 0l103.49 103.49c30.13 30.13 30.13 79.17 0 109.3L425.38 689.42 212.6 476.63l333.75-333.76zM188.18 565.42L336.6 713.84l-163.14 14.72 14.72-163.14zM928.96 902.94H95.71c-22.11 0-40.03 17.93-40.03 40.03S73.6 983 95.71 983h833.25c22.11 0 40.03-17.93 40.03-40.03s-17.91-40.03-40.03-40.03z" fill="#ffffff" p-id="24666"></path></svg>
        </i>
        <span>反馈</span>
    </a>
    <a href="javascript:;" class="goTopNew" onclick="toTop()">
        <i>
            <svg t="1616483711318" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="58737" width="16" height="16"><path d="M896.149659 67.771523 126.54051 67.771523c-34.758642 0-62.935378 28.176736-62.935378 62.935378 0 34.757618 28.176736 62.934355 62.935378 62.934355l769.610172 0c34.758642 0 62.935378-28.176736 62.935378-62.934355C959.085036 95.948259 930.9083 67.771523 896.149659 67.771523zM557.654294 258.83814c-1.471514-1.470491-3.016707-2.862187-4.625344-4.181229-0.713244-0.586354-1.469468-1.095961-2.202155-1.6465-0.906649-0.681522-1.797949-1.384533-2.743484-2.01796-0.884137-0.591471-1.805112-1.105171-2.713808-1.648546-0.853437-0.509606-1.689479-1.044796-2.568499-1.515516-0.928139-0.496304-1.883907-0.917906-2.832512-1.364067-0.913812-0.431835-1.811252-0.886183-2.746554-1.27504-0.924045-0.382717-1.864464-0.689708-2.800789-1.02433-1.000793-0.36225-1.989307-0.744967-3.012613-1.054005-0.938372-0.283456-1.892093-0.491187-2.837628-0.729617-1.043772-0.264013-2.071172-0.554632-3.133364-0.766456-1.094938-0.215918-2.201132-0.344854-3.305279-0.503467-0.927115-0.13303-1.840928-0.309038-2.78237-0.402159-2.059915-0.201591-4.124947-0.311085-6.192026-0.312108-0.005117 0-0.011256 0-0.016373 0l0 0c-0.299829 0-0.599657 0.037862-0.898463 0.041956-16.406668-0.231267-32.884968 5.874801-45.402049 18.391882L148.569222 577.09967c-24.576745 24.578792-24.576745 64.425312 0 89.005127 12.288884 12.289907 28.396747 18.434861 44.502563 18.434861 16.105816 0 32.213679-6.144954 44.502563-18.434861l212.633818-212.634842L450.208167 893.124254c0 34.757618 28.176736 62.934355 62.934355 62.934355 34.758642 0 62.935378-28.176736 62.935378-62.934355L576.077899 455.269951l210.836893 210.834846c12.288884 12.289907 28.395724 18.434861 44.500517 18.434861 16.10684 0 32.212656-6.144954 44.500517-18.434861 24.580838-24.579815 24.580838-64.426335 0-89.005127L557.654294 258.83814z" p-id="58738" fill="#ffffff"></path></svg>
        </i>
        <span>顶部</span>
    </a>
</div>


<script language="javascript">
    function toTop() {
        T.startMoveScrollTop(3,0 );
    }
</script>
<script>
    $(function(){

        //新版返回顶部侧栏二维码
        $(".jq_downBtn").click(function(){
            var _this = this;
            var fixedEwm = $(".jq_fixedEwm");
            if(fixedEwm.hasClass("animate")){
                fixedEwm.removeClass("animate");
                $(_this).removeClass("active");
            }else{
                fixedEwm.addClass("animate");
                $(_this).addClass("active");
            }
        })

        //客服时间
        $(".jq_kf").hover(function(){
            var _this = this;
            $(_this).addClass("hover");
        },function(){
            $(this).removeClass("hover");
        })
        /*反馈按钮*/
        goFeedBack = function () {
            checkLogin(function (data) {
                window.location.href = 'https://www.ttzoushi.com'+"/feedback";
            },function (data) {
                loadLogin();
            })
        }



    })
</script>

<script type="text/javascript" src="https://r.ttyingqiu.com/r/js/??common/web/footer.js,common/web/QRCode.js?v=20230717004"></script>
<script>
	$(function () {
		// 隐藏管家二维码
		/*if (checkHiddenQrcode()){
            if($("#kfTxt_qrcode").length>0){
                $("#kfTxt_qrcode").hide();
                $("#kfTxt_phone").css('padding-top','6px');
            }
        }*/

		$.ajax({
			url: "https://www.ttzoushi.com/const/config",
			type: "GET",
			dataType: "jsonp",
			success: function (data) {
				if (data.isSuccess && data.promotion) {
					var _tel = data.promotion.tel;
					if($("#kf_header").length > 0){
						$("#kf_header").text("(" + _tel.substr(0, 4) + ") " + _tel.substr(4,8));
					}
					if ($("#kfTxt_phone").length > 0) {
						$("#kfTxt_phone").text("(" + _tel.substr(0, 4) + ") " + _tel.substr(4,8));
					}
					if ($("div.butler img").length > 0) {
						$("div.butler img").attr("src", data.promotion.qrCode)
					}
					if ($("div.wxSlideWrap img").length > 0) {
						$("div.wxSlideWrap img").attr("src", data.promotion.qrCode)
					}
					if($("#kf_phone").length>0){
						$("#kf_phone").text("客服电话：(" + _tel.substr(0, 4) + ") " + _tel.substr(4,8));
					}
					if($("div.goFixedNew div.kfTxt img").length>0){
						$("div.goFixedNew div.kfTxt img").attr("src",data.promotion.qrCode)
					}
					if($("#error-popupPay").length>0){
						$("#error-popupPay div.ewm img").attr("src",data.promotion.qrCode)
						if($("#payInfo_phone").length>0){
							$("#payInfo_phone").text("客服电话：(" + _tel.substr(0, 4) + ") " + _tel.substr(4,8));
						}
					}
				}
			}
		});
	})
/*	var aiFlag = window.location.href;
	if(aiFlag != null &&(aiFlag.toLowerCase().indexOf("kaijiang")==-1 && aiFlag.toLowerCase().indexOf("kjgg")==-1
		&& aiFlag.toLowerCase().indexOf("zst")==-1 && aiFlag.toLowerCase().indexOf("download")==-1)){*/
	/*var isAicai = ;
	if(isAicai===undefined)
	    isAicai = false;
	var isNewDomain = ;
	if(isNewDomain===undefined)
		isNewDomain = false;*/
	

		var _hmt = _hmt || [];
		(function() {
		  var hm = document.createElement("script");
		  hm.src = "https://hm.baidu.com/hm.js?3914bc5cc7a483c3b70e7b052622b558";
		  var s = document.getElementsByTagName("script")[0]; 
		  s.parentNode.insertBefore(hm, s);
		})();

	//}

</script>
<!-- <script src="http://s11.cnzz.com/z_stat.php?id=1261104076&web_id=1261104076" language="JavaScript"></script> -->
<script type="text/javascript">
	$(function (){
		checkUUID();
		// var firstStart = window.sessionStorage.getItem('firstStart');
		var firstStart = getCookieValByLogin('firstStart');

		if(!firstStart) {
			getDataList();
		}
	})

	function getDataList() {
		/*var platform = 'web';
		var host = location.host;
		if(host.indexOf("ttzoushi")!=-1) {
			platform = 'ttzsweb'
		}*/

		var host = location.host;
		var toUrl = '//www.ttyingqiu.com/web/start';
		if(host.indexOf("ttzoushi")!=-1) {
			toUrl = '//www.ttzoushi.com/web/start'
		}else if(host.indexOf("yingti666")!=-1){
			toUrl = '//www.yingti666.com/web/start'
		}

		$.ajax({
			type: 'GET',
			url: toUrl,
			// data:'platform='+platform,
			dataType: 'jsonp',
			success: function (data) {
				// var result = JSON.parse(data);
				if(data.success) {
					// console.log("firstStart");
					// window.sessionStorage.setItem('firstStart','true');
					var _host = location.host.substring(location.host.indexOf("."));
					
					document.cookie = 'firstStart' + "=" + encodeURIComponent('true') + "; path=" + "/" + "; domain=" + _host ;
				}
			}
		})
	}

	function getCookieValByLogin(name) {
		var cookieArr = document.cookie.replace(/\s/g, "").split(';');
		for ( var i = 0; i < cookieArr.length; i++) {
			var tempObj = cookieArr[i].split('=');
			if (tempObj[0] == name)
				return decodeURIComponent(tempObj[1]);
		}
		return null;
	}

	function setCookieByLogin (name, value, expires) {
		var _host = window.location.host;
		_host = _host.substring(location.host.indexOf("."));
		if (typeof (expires) == 'undefiend' || expires == null || expires == '') {
			document.cookie = name + "=" + encodeURIComponent(value) + "; path=" + "/" + "; domain=" + _host ;
		} else {
			var expTimes = expires * 1000;
			var expDate = new Date();
			expDate.setTime(expDate.getTime() + expTimes);
			document.cookie = name + "=" + encodeURIComponent(value)
					+ ";expires=" + expDate.toGMTString() + "; path=" + "/"
					+ "; domain=" + _host ;
		}
	}

	function getUUID(){
		return 'VUID'+new Date().getTime()+""+Math.ceil(Math.random()*(999999-100000)+100000);
	}

	function checkUUID(){
		var uuid = getCookieValByLogin('VUID');
		if(typeof (uuid) == "undefined" || uuid == "" || typeof (uuid)!= "string" || uuid == null){
			uuid = getUUID();
			setCookieByLogin('VUID',uuid,365*24*60*60);
		}
	}
</script>

<div style="display:none;"><a href="http://www.anquan.org/s/www.aicai.com" name="TVzzKcc7nwgD3j8mVeXjd4OTn9gCbykv9oHbybkacKRgApQDEe">安全联盟</a></div>

<script type="text/javascript" src="https://r.ttyingqiu.com/r/js/??zst/analysis/dlt/dlt_util.js?v=20230717004"></script>
<div class="ui_dialog_wrap" id=""><div class="ui_dialog" style=""><table class=""><tbody><tr><td class="ui_border r0d0"></td><td class="ui_border r0d1"></td><td class="ui_border r0d2"></td></tr><tr><td class="ui_border r1d0"></td><td><table class="ui_dialog_main"><tbody><tr><td class="ui_title_wrap"><div class="ui_title"><div class="ui_title_text"></div><a class="ui_close" href="javascript:void(0)">×</a></div></td></tr><tr><td class="ui_content_wrap" style="width: auto; height: auto;"><div class="ui_content " id=""></div></td></tr><tr><td class="ui_bottom_wrap"><div class="ui_bottom"><div class="ui_btns"></div><div class="ui_resize"></div></div></td></tr></tbody></table></td><td class="ui_border r1d2"></td></tr><tr><td class="ui_border r2d0"></td><td class="ui_border r2d1"></td><td class="ui_border r2d2"></td></tr></tbody></table></div></div></body><chatgpt-sidebar data-gpts-theme="light"></chatgpt-sidebar><chatgpt-sidebar-popups data-gpts-theme="light"></chatgpt-sidebar-popups></html>
