---

layout: home
---
<head>
    <meta charset="utf-8">
    <link rel="icon" type="image/x-icon" href="img/favicon/favicon.ico"/>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="robots" content="follow,index">
    <META NAME="Title" CONTENT="Cloud ">
    <META NAME="Keywords" CONTENT="aws, azure, gcp, csp, cloud, cloud service provider, cloud computing, cloud services">
    <META NAME="Description" CONTENT="Mapping of services offered by Public Cloud Service Providers">
    <META NAME="Author" CONTENT="Abrom Douglas III">
    <link rel="canonical" href="https://cloud.abrom.dev/">
    <title>Cloud Service Providers | AWS, Azure, & GCP</title>
</head>
<table id="cloudservices">
  <tr align="center" class="header">
	<th style="width:7%">Category</th>
    <th style="width:10%">Service</th>
    <th><img  src="img/csp_logos/aws.svg" alt="AWS Logo" class="csp-logo"/></th>
	<th><img  src="img/csp_logos/azure.svg" alt="Azure Logo" class="csp-logo"/></th>
	<th><img  src="img/csp_logos/gcp.svg" alt="GCP Logo" class="csp-logo"/></th>
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