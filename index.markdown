---

layout: home
---
<head>
    <meta charset="utf-8">
    <link rel="icon" type="image/x-icon" href="img/favicon/favicon.ico"/>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <META NAME="Keywords" CONTENT="aws, azure, gcp, csp, cloud, cloud service provider, cloud computing, cloud services">
    <META NAME="Description" CONTENT="Mapping of services offered by Public Cloud Service Providers">
    <META NAME="Author" CONTENT="Abrom Douglas III">
    <link rel="canonical" href="https://learncloud.today/">
    <title>LearnCloud.today</title>
</head>
<!-- ========================= addthis sharing ========================= -->
<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-63d59243da3cfde4"></script>
<!-- ========================= intro info ========================= -->
<table id="intro" style="margin-bottom: 30px; width: 100%; text-align: left; color: #3f3f3f; border-collapse: collapse;">
	<th style="font-size: 1vw; width:80%">
	"Text here"
	</th>
	<th style="width:20%">
		<a href="https://github.com/iamabrom" target="_blank"> <img src="https://badgen.net/badge/icon/Follow @iamAbrom?icon=github&label&scale=1.2"></a><br>
    	<a href="https://github.com/iamabrom/learncloud.today" target="_blank"> <img src="https://badgen.net/github/stars/iamabrom/learncloud.today?scale=1.2"></a><br>
    	<a href="https://github.com/iamabrom/learncloud.today" target="_blank"> <img src="https://badgen.net/github/issues/iamabrom/learncloud.today?scale=1.2"></a><br>
		<hr style="height:2px; border-width:0; color:gray; background-color:gray;">
    	<a href="https://authn.cc/@abrom" target="_blank"> <img src="https://badgen.net/badge/icon/@abrom@authn.cc/purple?icon=mastodon&label&scale=1.2"></a><br>
    	<a href="https://twitter.com/iamAbrom" target="_blank"> <img src="https://badgen.net/badge/icon/@iamAbrom?icon=twitter&label&scale=1.2"></a><br>
    	<a href="https://www.buymeacoffee.com/abrom" target="_blank"> <img src="https://badgen.net/badge/icon/buymeacoffee/yellow?icon=buymeacoffee&label&scale=1.2"></a>
	</th>
</table>
<!-- ========================= mapping table ========================= -->
<table id="cloudservices">
  <tr align="center" style="position: sticky; top: 0; z-index: 1;" class="header">
	<th style="font-size: 1.30vw; width:10%">Category</th>
    <th style="font-size: 1.30vw; width:10%">Service</th>
    <th><img  src="img/csp_logos/aws.svg" alt="AWS Logo" class="awslogo"/></th>
	<th><img  src="img/csp_logos/azure.svg" alt="Azure Logo" class="azurelogo"/></th>
	<th><img  src="img/csp_logos/gcp.svg" alt="GCP Logo" class="gcplogo"/></th>
  </tr>
	{% for item in site.data.cspdata.services %}
	<tr>
		<td>{{item.category}}</td>
		<td>{{item.subcategory}}</td>
		<td>
			<ul>
			    {% for entry in item.service %} 
					{% for record in entry.aws %}
						<li ><img src="img/icons/aws/{{record.icon}}" alt="{{record.name}}" > <a href="{{record.link}}" target="_blank" alt="{{record.name}}">{{record.name}}</a></li>
					{% endfor %}	
				{% endfor %}	
			</ul>
		</td>
		<td>
			<ul>
			    {% for entry in item.service %} 
					{% for record in entry.azure %}
						<li><img src="img/icons/azure/{{record.icon}}" alt="{{record.name}}"  ><a href="{{record.link}}" target="_blank" alt="{{record.name}}">{{record.name}}</a></li>
					{% endfor %}	
				{% endfor %}	
			</ul>
		</td>
		<td>
			<ul>
			    {% for entry in item.service %} 
				{% for record in entry.google %}
					<li><img src="img/icons/gcp/{{record.icon}}" alt="{{record.name}}" ><a href="{{record.link}}" target="_blank" alt="{{record.name}}">{{record.name}}</a></li>
				{% endfor %}	
				{% endfor %}	
			</ul>
		</td>
	</tr>
	{% endfor %}
</table>