---
layout: default
---

<section id="intro" class="flex-center">
	<div class="text-container center">
      <h1>Hi! I'm Anna, a UX UI Designer </h1>
		<a href="dokumente/broschuere.pdf" download="broschuere.pdf">Broschüre herunterladen</a>
		<a href="Anna_Vasilevich_lebenslauf_2024.pdf" target="_blank">MY CV</a> 
       <!--<p> My goal is to empower users through interfaces that enhance their interactions. <br> I'm driven by the belief that design should be accessible, intuitive, and enjoyable for all.</p>-->
      <div class="skills">
      	{% for skill in site.skills %}
      		<image src="/assets/skills/{{skill}}.png"/>
      	{% endfor %}
      </div>
      <div id="social-links">
      	<a href="https://www.behance.net/annavasilevich" target="_blank"><image src="/assets/social/Icon_awesome-behance-square.png"/></a>
      	<a href="https://www.linkedin.com/in/anna-vasilevich1627/" target="_blank"><image src="/assets/social/Icon_awesome-linkedin.png"/></a>
      <!--<a href="https://www.behance.net/annavasilevich" target="_blank"><image src="/assets/social/Icon_instagramm.png"/></a>  -->
      </div>
	</div>
</section>
<section id="portfolio">
	<div class="section-title">
		<h2>Portfolio</h2>
	</div>
	<div class="wrapper">
		<div class="columns-2">
		{% assign projects = site.projects | sort: "order" %}
		{% for project in projects %}
			  	<a class="project" href="{{ project.url }}" style="box-shadow: -3px 15px 20px 6px #8249491a;">
					<div class="project-image hover-seen">
						<image src="/assets/projects/{{ project.handle }}/{{ project.hoverPreview }}"/>
					</div>
					<div class="project-image hover-hidden">
						<div class="skills">
							{% for skill in project.skills %}
								<image src="/assets/skills/{{skill}}.png"/>
							{% endfor %}
						</div>
						<image src="/assets/projects/{{ project.handle }}/{{ project.primaryPreview }}"/>
					</div>
					<span class="button hover-hidden" href="{{ project.url }}">
						<span>{{ project.displayName }}</span>
					</span>
					<span class="button hover-seen" href="{{ project.url }}">
						<span>
							See more &nbsp;&nbsp;
							<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 43.665 43.665">
							  <g id="Icon_feather-arrow-up-right" data-name="Icon feather-arrow-up-right" transform="translate(21.894 2.828) rotate(45)">
								<path id="Pfad_5" data-name="Pfad 5" d="M0,28.962a1.994,1.994,0,0,1-1.41-.581,2,2,0,0,1-.009-2.828L25.371-1.41A2,2,0,0,1,28.2-1.419a2,2,0,0,1,.009,2.828L1.419,28.372A1.994,1.994,0,0,1,0,28.962Z" fill="#824949"/>
								<path id="Pfad_6" data-name="Pfad 6" d="M26.79,28.962a2,2,0,0,1-2-2V2H0A2,2,0,0,1-2,0,2,2,0,0,1,0-2H26.79a2,2,0,0,1,2,2V26.962A2,2,0,0,1,26.79,28.962Z" fill="#824949"/>
							  </g>
							</svg>
						</span>
					</span>
				</a>
		{% endfor %}
		</div><!-- ./columns-2 -->
	</div><!-- ./wrapper -->
</section>
