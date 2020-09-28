--- 
layout: post
title: "SEO: Use Images Wisely"
created: 1078657560
categories: 
- validation
- SEO
- img
- longdesc
- alt
- Search Engine Voodoo
---
<p>
	As part of <a href="/node/917" title="Search Engine Voodoo - Validate Your Code">validation</a>, you may have noticed warnings if you failed to add <code>alt</code> attributes to your <code>img</code> tags. The <code>alt</code> attribute isn&#39;t there just to conform to a standard - it&#39;s actually useful! It stands for &quot;alternative&quot; and can be used to add a textual description to any image. As we&#39;ve discussed earlier, search engines are blind, so this description is vital for letting search engines know what your image represents.</p>
<!--break-->
<p>
	A picture of a kitten might have an <code>alt</code> attribute as follows:</p>
<blockquote class="code">
	&lt;img src=&quot;kitten.jpg&quot; alt=&quot;A white Persian kitten&quot; /&gt;</blockquote>
<p>
	A search engine would then associate the file <code>kitten.jpg</code> with the text &quot;A white Persian kitty&quot;.</p>
<p>
	Additionally, the <code>title</code> attribute can be used to add text that acts as a caption for an image. Continuing with the previous example, we might use the following text:</p>
<blockquote class="code">
	&lt;img src=&quot;kitten.jpg&quot; alt=&quot;A white Persian kitten&quot; title=&quot;Allie&#39;s Kitten&quot; /&gt;</blockquote>
<p>
	Now we&#39;ve given the image a short descriptive phrase (<code>alt</code>) as well as a caption (<code>title</code>). The title attribute can actually be used for other elements as well, including the anchor tag. Many browsers will show the text of the <code>title</code> attribute in a floating &quot;tool tip&quot; box when the mouse pointer is placed over the element.</p>
<p>
	If you really want to go overboard, you can consider using the <code>longdesc</code> attribute, which is for including descriptive text that is too long to fit into the <code>alt</code> attribute.</p>
<p>
	But back to the wise use of images. Just as a page filled with images won&#39;t be very useful for a blind person, a search engine won&#39;t care much either. The critical portions of a page that should never be replaced with images are the various headings, company names, and pull quotes. While it is understandable to want to make these areas visually appealing, a search engine won&#39;t be able to &quot;read&quot; any text that appears in these graphics.</p>
<!-- aside: press releases as images, PDFs --><p>
	Two options exist. One is to use stylesheets to apply styling to text to make it standout. The second is to use one of a number of CSS tricks to replace the text with graphics (the most common one probably being the Fahrner Image Replacement [FIR] technique).</p>
<p>
	What&#39;s that? You&#39;re still not convinced? You want pretty looking graphics, or exact control over how content is going to appear? Let me go back to what I said earlier: search engines can&#39;t read graphics. Now let&#39;s imagine that your marketing department decides to start releasing press releases as images, or PDFs. Well, if the whole press release is a graphic, the entire contents of the press release will be invisible as far as the web is concerned.</p>
<p>
	PDFs are slightly better (Google, for example, can read the text inside of PDFs) but consider users that don&#39;t have a PDF reader installed. Or those browsing the web on handheld devices. Don&#39;t make things harder than they have to be! If you can generate a PDF, you can generate an HTML page of the press release.</p>
