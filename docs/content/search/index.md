---
date: 2017-05-17T11:11:46+02:00
title: Search
---

## Search content within the documentation

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>Search</title>

<link rel="stylesheet" href="/tipuesearch/css/normalize.css">

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>

<script type="text/javascript" src="/tipuesearch/tipuesearch_content.js"></script>
<link rel="stylesheet" type="text/css" href="/tipuesearch/css/tipuesearch.css">
<script type="text/javascript" src="/tipuesearch/tipuesearch_set.js"></script>
<script type="text/javascript" src="/tipuesearch/tipuesearch.min.js"></script>

<link rel="stylesheet" href="/css/animated_search_bar.css">

<form action="#">
	<div class="tipue_search_left"><img src="/tipuesearch/search.png" class="tipue_search_icon"></div>
	<div class="tipue_search_right"><input type="text" name="q" id="tipue_search_input" pattern=".{3,}" title="At least 3 characters" placeholder="(at least 3 characters)" required></div>
	<div style="clear: both;"></div>
</form>

<div id="tipue_search_content"></div>

<script>
$(document).ready(function() {
     $('#tipue_search_input').tipuesearch({
          'mode': 'live'
     });
});
</script>
