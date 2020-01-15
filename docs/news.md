<style>h1{display:none}</style>
<div class="ui segment" id="progress" style="padding-top:30px;">
  <div class="ui active inverted dimmer">
    <div class="ui text loader">Loading news from Twitter...</div>
  </div>
  <div class="ui placeholder">
	  <div class="image header">
    		<div class="line"></div>
   		<div class="line"></div>
 	 </div>
 	 <div class="image header">
    		<div class="line"></div>
   		<div class="line"></div>
 	 </div>
 	 <div class="image header">
    		<div class="line"></div>
   		<div class="line"></div>
 	 </div>
 	 <div class="image header">
    		<div class="line"></div>
   		<div class="line"></div>
 	 </div>
 	 <div class="image header">
    		<div class="line"></div>
   		<div class="line"></div>
 	 </div>
 	 <div class="image header">
    		<div class="line"></div>
   		<div class="line"></div>
 	 </div>
 	 
  </div>  
</div>

<div style="display:none" id="news">
<a class="twitter-timeline" href="https://twitter.com/nextedy?ref_src=twsrc%5Etfw">Tweets by nextedy</a>
</div> 
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<script>

function setSizes(){
			console.log("setting style ...");
   			var style = "<p>.</p><style>.timeline-Tweet-text{font-size:	17px !important;line-height:26px !important;margin-bottom:10px !important;margin-left:5px !important;white-space:normal !important} .timeline-Tweet-media{font-size:	16px !important;} .timeline-Tweet-author{display:none;} .u-floatRight{margin-right: 5px;float: left!important;} </style>";
	    		$("#progress").hide();
			$("#news").show();
			$(".twitter-timeline").contents().find(".timeline-Widget").first().prepend(style);
			console.log("setting style DONE");
}

var i = 0;
var findTweet = function(){
	i++;
	console.log("search tweet:"+i);
	var loaded = $(".twitter-timeline").contents().find(".timeline-Tweet").length;
	console.log(" - " + loaded + " tweets found.");	
    if(loaded>0){
	    		setTimeout(setSizes, 200); 	 	
    }else {
    		if(i<100){
	    		setTimeout(findTweet, 100); 	 	
    		}else{
    			$("#progress").hide();
			$("#news").show();
    		}
    }
}
$(window).bind("load", findTweet);
</script>

## Product Changes

* [{{ product.name}} Change log](../changelog)

