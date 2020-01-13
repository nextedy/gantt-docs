<style>h1{display:none}</style>
<div class="ui segment" id="progress" style="padding-top:30px;">
  <div class="ui active inverted dimmer">
    <div class="ui text loader">Loading</div>
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
   var tweetStyles = {
      "font-size":	 "16px",
      "line-height": "24px",
      "margin-bottom": "10px",
      "margin-left": "5px",
      "white-space": "normal"
    };
	    		$("#progress").hide();
			$("#news").show();
			$(".twitter-timeline").contents().find(".timeline-Tweet-text").css(tweetStyles);
			$(".twitter-timeline").contents().find(".timeline-Tweet-media").css("font-size","14px");
			$(".twitter-timeline").contents().find(".timeline-Tweet-author").hide();	
			$(".twitter-timeline").contents().find(".timeline-Footer").hide();							
}

var i = 0;
var findTweet = function(){
	i++;
	console.log("search tweet:"+i);
	var tweet = $(".twitter-timeline").contents().find(".timeline-Tweet-text").first();
    if(tweet!=null){
	    		setTimeout(setSizes, 100); 	 	
    }else {
    		if(i<100){
	    		setTimeout(findTweet, 100); 	 	
    		}
    }
}
$(window).bind("load", findTweet);
</script>

## Old index
* [Change log](../changelog)

