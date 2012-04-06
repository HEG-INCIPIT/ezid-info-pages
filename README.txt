The HTML files in this folder contain the HTML for the main parts
of the page for the mostly static informational pages.  These are
in a separate "ezid-info-pages" Mercurial repository and are in the
SITE/templates/info folder in the EZID site's file system.

The each file has 3 special blocks which control the way content
appears.  The blocks do not need to be changed, but HTML text
may be filled in or changed between the block and endblock
tags for each.

The title block -- Fill in the desired page title here. The
title is what will appear as the title in the web browsers
title bar.

The main_column block -- Fill in HTML that will appear in the
large, left main column of the interface.

The sidebar block -- Fill in any HTML to be displayed in the
sidebar space on the right side of hte page.  The sidebar
may be left off or left empty if it doesn't need to be displayed.

The "extends" directive at the top of the file should be left alone.

A simple example with a small amount of HTML content:
-----------------------------------------------------

{% extends "layouts/information.html" %}

{% block title %}My EZID Test Page{% endblock %}

{% block main_column %}

	<h1>My EZID Test Page</h1>
	
	<p>
		I'm testing out working with EZID. Lorem ipsum dolor sit amet,
		consectetur adipiscing elit. Curabitur sit amet dolor lorem,
		vitae laoreet dui. Cras id magna nulla, ut sodales mi.
		Aliquam et felis massa.
	</p>
	
{% endblock %}

{% block sidebar %}
	<h1>Supplemental Information</h1>
	
	<p>EZID is great because</p>
	
	<ul>
		<li>It makes the best IDs ever</li>
		<li>It lets you associate metadata with IDs</li>
		<li>You can look things up in a consistent way</li>
	</ul>
	
	<p>If you love it, <a href="mailto:dummy.test@ucop.edu">let us know</a>!</p>
{% endblock %}