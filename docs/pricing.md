#  Pricing FAQ


## 1. How much does the "{{product.name}}" license cost?

No haggle  - Our pricing is simple, fair and transparent.

Your purchase entitles you to **perpetual use** of the software 
(pay once and use a program indefinitely).

It includes **12 months of software support** & maintenance. 

The *{{product.name}}* pricing is based on **size** of the Polarion deployment, the more users are on the server, the bigger is a price.  We count all active users on the Polarion server. An active **user is** by definition any user account in the Polarion system with the global role  *"User"*, i.e., **anyone who can log in** to Polarion portal.


<center>

**Number of users**  	| **Price**
------------------- 	| -------------
1-10 users			|  245 EUR		
11-25 users			|  460 EUR
26-50 users			|  690 EUR	
51-100 users			| 1040 EUR		
101-250 users		| 1950 EUR
251-500 users		| 2930 EUR
501-1000 users		| 3700 EUR	
1001-2500 users		| 4500 EUR	
2501+ users			| 5000 EUR


<br/>
<a href="#getquote">
<button class="mdc-button">&nbsp;Get official Quote!&nbsp;</button>
</a>
</center>

<div class="who-banner" >
<b><i>Why to pay and not develop in house?</i></b>
<p>
Our experts bring the 14 years experience of design and implementation of various customizations while remaining aligned to core Polarion principles.
</p>
<p>
The <b>usability</b> and <b>performance</b> is not an afterthought, but considered right from the early design phases.
</p>
<p>
We maintain the plugins for big number of Polarion customers, with  <b>Support & Maintenance</b> contract we guarantee that the plugins keep working well in the future.
</p>
</div>

## 2. What is covered by Support & Maintenance?

Software Support & Maintenance, included in first 12 months from the date of purchase, covers the following benefits:

* Critical **bug fixes**
* Update to **new versions** of the SW and benefit from new features & enhancements
* Access our experienced Support team for **technical troubleshooting**
* **Staging server** license key (to be requested separately)
* Optional participation in **Early Access Programs**

While renewing your software maintenance annually is optional, it is strongly encouraged in order to ensure continuous access to all of the benefits listed above. 

## 3. How much is it to renew support & maintenance contract?

Subsequent maintenance price is **30%** of base perpetual license price. 

We automatically send a no-obligation quote 90 days before the maintenance is to expire on a license.

Software maintenance renewals commence from the expiration of your active maintenance period, regardless of when the maintenance renewal is purchased. If you intend to renew, we recommend renewing at least 30 days before expiration.


## 4. What are the license terms?
A valid commercial license entitles you to:

* Install *{{product.name}}* Software on a single instance in a production environment on **1 Polarion server** (including load balanced clustered server)
* **Perpetual (time unlimited)** use of *{{product.name}}* Software
* Benefit from Software Support & Maintenance for 12 months - including all updates and online support

Licensing fees are quoted per number of 'active users.' An active **user is** by definition any user account in the Polarion system with the global role  *"User"*, i.e., **anyone who can log in** to Polarion portal.

Detailed conditions available [here]({{product.url}}/download/LICENSE.pdf).

## 5. Is there trial license available 

The evaluation license is included in the distribution. You can download the product and **evaluate** it free of charge for **30 days**.

<a name="getquote">&nbsp;</a>

## 6. How do I purchase a license?

Start by requesting a no-obligation quote valid for next 30 days:

<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "{{hs.id}}",
	formId: "{{hs.quoteFormId}}"
});
</script>


### Cannot get a quote?

We have experienced that some privacy browser add-ons are blocking our CRM System HubSpot (Although we  follow the privacy recommendations and we support GDPR standard). 
	
	
If you cannot submit the quote form from our website - please write us an email to <a href="mailto:info@nextedy.com">info@nextedy.com</a>
 

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






