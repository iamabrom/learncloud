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
<table id="intro" style="margin-bottom: 30px; width: 100%; text-align: left; color: #3f3f3f; border-collapse: collapse; background-color: #252833; color:white; font-size: 1.1vw">
<tr>
    <td>
      <p>Welcome to LearnCloud.today!</p>
      <p>The first iteration of this site is to soley provide visibility and a mapping of services offered across AWS, Azure, & GCP. Soon to follow will be articles, thought leadership posts, technical whitepapers, and even reference architectures.</p>
      <p>Show support by staring the Github repo and </p>
    </td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/iamabrom" target="_blank"> <img style="height:1.5em; width:auto;" src="https://img.shields.io/github/followers/iamabrom?label=Follow%20%40iamAbrom&style=social"></a>
      <a href="https://github.com/iamabrom/learncloud" target="_blank"> <img style="height:1.5em; width:auto;" src="https://img.shields.io/github/stars/iamabrom/learncloud?label=Repo%20Stars&style=social"></a>
      <a href="https://github.com/iamabrom/learncloud/issues" target="_blank"> <img style="height:1.5em; width:auto;" src="https://img.shields.io/github/issues-raw/iamabrom/learncloud"></a><br>
      <a href="https://authn.cc/@abrom" target="_blank"> <img style="height:1.2em; width:auto;" src="https://img.shields.io/mastodon/follow/109379946434563076?domain=https%3A%2F%2Fauthn.cc&style=social"></a>
      <a href="https://twitter.com/iamAbrom" target="_blank"> <img style="height:1.2em; width:auto;" src="https://img.shields.io/twitter/follow/iamabrom?style=social"></a>
      <a href="https://www.buymeacoffee.com/abrom" target="_blank"> <img style="height:1.2em; width:auto;" src="https://badgen.net/badge/icon/Buy me a coffee/yellow?icon=buymeacoffee&label"></a>
    </td>
  </tr>
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