---
layout: page
title: Projects
permalink: /projects/
---

This is a community-generated list of software projects developed at UC Davis.

Please add your projects to this list **regardless of whether the source code is available** or
the project is open for reuse.

The purpose of this list is multi-factored:

* Discover what project categories have been worked on
* Discover what technology stacks (language, frameworks, etc.) are being used on campus
* Discover what development teams exist on campus
* Encourage project collaboration and re-use as allowed
* Encourage the open source philosophy as allowed

<table class="table-fill">
	<thead>
		<th>
			Name
		</th>
		<th>
			Team
		</th>
		<th>
			Description
		</th>
		<th>
			Technologies
		</th>
		<th>
			URL
		</th>
		<th>
			Source
		</th>
		<th>
			Contact
		</th>
	</thead>
	<tbody class="table-hover">
		{% for project in site.projects %}
			<tr>
				<td>{{ project.name }}</td>
				<td>{{ project.team }}</td>
				<td>{{ project.description }}</td>
				<td>{{ project.technologies }}</td>
				<td>{{ project.public_url }}</td>
				<td>{{ project.repo_url }}</td>
				<td>{{ project.contact }}</td>
			</tr>
		{% endfor %}
	</tbody>
</table>
