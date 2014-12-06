<!DOCTYPE html>
<html>
        <head>
                <title>{Title}</title>
        </head>
        <body>
                <header><a href="{Title}">{Title}</a></header>
        	{block:Posts}
	
		{block:Text}
		<div class="post">
		<div class="title">
			{block:Title}
			</div>
				<h3>
					<a href="{Permalink}">{Title}</a>
				</h3>
			{/block:Title}
			{Body}
			<ul class="like-reblog">
				<li>{LikeButton}</li>
				<li>{ReblogButton}</li>
				<li>{block:NoteCount}<a href="{Permalink}#notes">{NoteCountWithLabel}</a>{/block:NoteCount}</li>
				<li>{block:Date}<a href="{Permalink}">{TimeAgo}</a>{/block:Date}</li>
			</ul>
		</div>
		{block:PostNotes}{PostNotes}{/block:PostNotes}
		{/block:Text}

		{block:Photo} 
		<div class="post">	
			<img src="{PhotoURL-500}">
			{block:Caption}{Caption}{/block:Caption}
			<ul class="like-reblog">
				<li>{LikeButton}</li>
				<li>{ReblogButton}</li>
				<li>{block:NoteCount}<a href="{Permalink}#notes">{NoteCountWithLabel}</a>{/block:NoteCount}</li>
				<li>{block:Date}<a href="{Permalink}">{TimeAgo}</a>{/block:Date}</li>
			</ul>
		</div>
		{block:PostNotes}{PostNotes}{/block:PostNotes}
		{/block:Photo}

		{block:Quote}
		<div class="post">
			{Quote}
	   	{block:Source}<br>&mdash;{Source}{/block:Source}
			<ul class="like-reblog">
				<li>{LikeButton}</li>
				<li>{ReblogButton}</li>
				<li>{block:NoteCount}<a href="{Permalink}#notes">{NoteCountWithLabel}</a>{/block:NoteCount}</li>
				<li>{block:Date}<a href="{Permalink}">{TimeAgo}</a>{/block:Date}</li>
			</ul>
		</div>
		{block:PostNotes}{PostNotes}{/block:PostNotes}
		{/block:Quote}

		{block:Link}
		<div class="post">
  			<a href="{URL}" {Target}>{Name}</a>
  			{block:Description}{Description}{/block:Description}
			<ul class="like-reblog">
				<li>{LikeButton}</li>
				<li>{ReblogButton}</li>
				<li>{block:NoteCount}<a href="{Permalink}#notes">{NoteCountWithLabel}</a>{/block:NoteCount}</li>
				<li>{block:Date}<a href="{Permalink}">{TimeAgo}</a>{/block:Date}</li>
			</ul>
		</div>
		{block:PostNotes}{PostNotes}{/block:PostNotes}
		{/block:Link}

		{block:Chat}
		<div class="post">
			{block:Title}{Title}{/block:Title}
			<table>
				{block:Lines}
				<tr>
					<th>{block:Label}{Label}{/block:Label}</th>
					<td>{Line}</td>
				</tr>
				{/block:Lines}
			</table>
			<ul class="like-reblog">
				<li>{LikeButton}</li>
				<li>{ReblogButton}</li>
				<li>{block:NoteCount}<a href="{Permalink}#notes">{NoteCountWithLabel}</a>{/block:NoteCount}</li>
				<li>{block:Date}<a href="{Permalink}">{TimeAgo}</a>{/block:Date}</li>
			</ul>
		</div>
		{block:PostNotes}{PostNotes}{/block:PostNotes}
		{/block:Chat}

		{block:Audio}
		<div class="post">
			{AudioPlayer}
      	{block:Caption}{Caption}{/block:Caption}
			<ul class="like-reblog">
				<li>{LikeButton}</li>
				<li>{ReblogButton}</li>
				<li>{block:NoteCount}<a href="{Permalink}#notes">{NoteCountWithLabel}</a>{/block:NoteCount}</li>
				<li>{block:Date}<a href="{Permalink}">{TimeAgo}</a>{/block:Date}</li>
			</ul>
		</div>
		{block:PostNotes}{PostNotes}{/block:PostNotes}
		{/block:Audio}

		{block:Video}
		<div class="post">
			{Video-500}
			{block:Caption}{Caption}{/block:Caption}
			<ul class="like-reblog">
				<li>{LikeButton}</li>
				<li>{ReblogButton}</li>
			<li>{block:NoteCount}<a href="{Permalink}#notes">{NoteCountWithLabel}</a>{/block:NoteCount}</li>
			<li>{block:Date}<a href="{Permalink}">{TimeAgo}</a>{/block:Date}</li>
			</ul>
		</div>
		{block:PostNotes}{PostNotes}{/block:PostNotes}
		{/block:Video}

	{/block:Posts}
	
	{block:Pagination}
    <div class="pagination">
        {block:NextPage}<a href="{NextPage}">Next page</a>{/block:NextPage}
        {block:PreviousPage}<a href="{PreviousPage}">Previous page</a> {/block:PreviousPage}
    </div>
    {/block:Pagination}
        </body>
</html>
