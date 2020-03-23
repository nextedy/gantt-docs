# Download {{product.name}}


## Installation Instructions

The installation instructions are available at the [support center]({{support.installGuide}}).
	
Installation requirements: <br/>&nbsp;&nbsp;&nbsp;*{{product.requirements}}*

## Download

Please fill in your email address to download the installation package.


<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "{{hs.id}}",
	formId: "{{hs.downloadFormId}}"
});
</script>


## Cannot download?

We have experienced that some privacy browser add-ons are blocking our CRM System HubSpot (Although we  follow the privacy recommendations and we support GDPR standard). 
	
	
If you cannot download the distribution from our website - please write us an email to <a href="mailto:info@nextedy.com">info@nextedy.com</a>
 
    

<script>
function setSizes(){
	console.log("setting style ...");
   	var style = "<style>.hubspot-link__container{display:none;}.submitted-message{border: 1px solid #ff7a59;padding: 10px;font-weight: bold;background-color: #ffe6e0;}.hs-input{background-color: white;border: 1px solid #f9bbac;}label{font-weight:bold;}legend{    color: #33475b !important;}</style>";
	$("#hs-form-iframe-0").contents().find(".hbspt-form").first().prepend(style);
	console.log("setting style DONE");
}
var i = 0;
var findHSForm = function(){
	i++;
	console.log("findHSForm:"+i);
	var loaded = $("#hs-form-iframe-0").contents().find(".hubspot-link__container").length;
	console.log(" - " + loaded + " hs form.");	
    if(loaded>0){
	    		setTimeout(setSizes, 10); 	 	
    }else {
    		if(i<100){
	    		setTimeout(findHSForm, 100); 	 	
    		}
    }
}
findHSForm();
</script>


