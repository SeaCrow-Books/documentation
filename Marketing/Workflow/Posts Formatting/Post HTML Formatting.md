
- [[#Example Tags|Example Tags]]
- [[#Headers|Headers]]
- [[#Paragraphs|Paragraphs]]
	- [[#Paragraphs#Lead|Lead]]
	- [[#Paragraphs#Inline Text Elements|Inline Text Elements]]
	- [[#Paragraphs#Positioning|Positioning]]
	- [[#Paragraphs#Links|Links]]
	- [[#Paragraphs#Lists|Lists]]
		- [[#Lists#Unordered List|Unordered List]]
		- [[#Lists#Ordered List|Ordered List]]
	- [[#Paragraphs#Additional Formatting|Additional Formatting]]
		- [[#Additional Formatting#Unstyled Lists|Unstyled Lists]]
		- [[#Additional Formatting#Inline List|Inline List]]
- [[#Blockquotes|Blockquotes]]
- [[#Images|Images]]
- [[#Iframes|Iframes]]
- [[#Alerts|Alerts]]
- [[#Table of Contents|Table of Contents]]
	- [[#Table of Contents#Part 1|Part 1]]
	- [[#Table of Contents#Part 2|Part 2]]
- [[#Frequently Asked Questions|Frequently Asked Questions]]
- [[#Semantic Elements|Semantic Elements]]


This is the guidelines for formatting tags and other elements when writing blog posts. It is important to have a basic understanding of HTML. In addition, an understanding of CSS would be helpful. 

Below is a list of resources that are referenced in this guide:
  
- This is the definitive resource for tags, if you have questions or just want to learn more consult this resource: [https://www.w3schools.com/TAGS/default.asp](https://www.w3schools.com/TAGS/default.asp)
- This is the framework that the SeaCrow site is built on: [https://getbootstrap.com/](https://getbootstrap.com/) 

The following resources will give you a basic understanding of HTML and CSS.

I would suggest you watch this short video for a basic understanding:

<iframe width="560" height="315" src="https://www.youtube.com/embed/salY_Sm6mv4?si=EZ-c-cY63zFcqzco" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


This longer video will give you a more complex breakdown: 

<iframe width="560" height="315" src="https://www.youtube.com/embed/qz0aGYrrlhU?si=XxlZ57wy7YnCaqvO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

To understand css, start here: 

<iframe width="560" height="315" src="https://www.youtube.com/embed/OEV8gMkCHXQ?si=ePy2onI2JNNxXXZS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

To gain an in depth knowledge, go take Odin Project free foundations course:  [https://www.theodinproject.com/paths/foundations/courses/foundations](https://www.theodinproject.com/paths/foundations/courses/foundations)    

## Example Tags

Below is a very basic example of the kinds of tags you will see in a blog post and how they are laid out. It is worth noting that many of the page tags are already hard coded into the website. 

The tags are not displayed in the final post and will be invisible to the reader, they are for the browser (and Google) to understand how a page is laid out.

```Copy
<h1>This is Main Title</h1>

<p class="example" id="another-example">This is text. Notice that it has been given a class and id, this allows it to be targeted by CSS and other languages, such as Javascript.</p>

<h2>This is a Subheader</h2>

<p>This is more paragraph text.</p>

<h3>This is a Sub-subheader</h3>

<div class="div-class">

	<p>This is text, notice how it is wrapped in a div with the class of 'div-class'. Also notice how it has been indented. This is not essential, but makes things easy to read.</p>
	
	<image>This is where you would put an image</image>

</div>

<ul>

	<li>This is a list item.</li>
	
	<li>This is another list item, it is part of an unordered list.<li>
	
	<li>This will be a bullet point list.</li>

</ul>

<ol>

	<li>This is a list item.</li>
	
	<li>This is another list item, it is part of an ordered list.<li>
	
	<li>This will be a numbered point list.</li>

</ol>
```
## Headers 

When adding a header DO NOT use a \<h1> tag. This is assigned automatically to the title of the blog post. Having more than one \<h1> tag will confuse Google, you should have one per page. 

Feel free to use \<h2>, \<h3>, \<h4>, \<h5> and \<h6> headers. However, these should be used sequentially. In other words:

\<h2>\Header 2 shows google this is the most important header after the title (h1).\</h2>
\<h3>\Header 3 is less important than Header 2.\</h3>
\<h4>Header 4 is less important than Header 3 and Header 2, and so on.\</h4>

A header should be given the title of "post-show__sub-title". This will allow them to be targeted by CSS. In most cases, you will not need to give additional classes.

It is important that such headers have an id, since this will allow the table of content below to work. For example:

``` Copy
<h2 class="post-show__sub-title" id="header-example">Header Example</h2>
```

## Paragraphs

Paragraph tags are the building blocks of the blog post. Here is an example:

\<p>This is an example of a paragraph. This can be as long as you need. This of these like paragraph breaks in Word.\</p>

As with all tags, you can add a class (and id). Below are examples of the classes that can be used, these are provided by Bootstrap. Click the link below to see an example of them in action.
[https://getbootstrap.com/docs/5.3/content/typography/](https://getbootstrap.com/docs/5.3/content/typography/)

### Lead

This creates a larger version of the text.

```Copy
<p class="lead">This is a lead paragraph. It stands out from regular paragraphs.</p>
```
### Inline Text Elements

These elements are part of the [Bootstrap system](https://getbootstrap.com/docs/5.3/getting-started/introduction/) and can be added to paragraphs.

```Copy

<p>You can use the mark tag to <mark>highlight</mark> text.</p>
<p><del>This line of text is meant to be treated as deleted text.</del></p>
<p><s>This line of text is meant to be treated as no longer accurate.</s></p>
<p><ins>This line of text is meant to be treated as an addition to the document.</ins></p>
<p><u>This line of text will render as underlined.</u></p>
<p><small>This line of text is meant to be treated as fine print.</small></p>
<p><strong>This line rendered as bold text.</strong></p>
<p><em>This line rendered as italicized text.</em></p>
```
<p>You can use the mark tag to <mark>highlight</mark> text.</p>
<p><del>This line of text is meant to be treated as deleted text.</del></p>
<p><s>This line of text is meant to be treated as no longer accurate.</s></p>
<p><ins>This line of text is meant to be treated as an addition to the document.</ins></p>
<p><u>This line of text will render as underlined.</u></p>
<p><small>This line of text is meant to be treated as fine print.</small></p>
<p><strong>This line rendered as bold text.</strong></p>
<p><em>This line rendered as italicized text.</em></p>

### Positioning 

By default the text will be positioned to the left hand side of the blog post, as in a book. However, it is possible to position either to the centre or left. To do this you use the class 'text-center' or 'text-right'.

Please note, that this should be used with caution. It is possible that the system CSS is already positioning the text (as with titles) and adding additional classes may either cause them to be ignored or moved in a way that is not wanted. CSS can get messy, remember it cascades and it is not always obvious which class will be expressed or overridden. 

```Copy

<p class="text-center">This is a block of text that will be moved to the centre of the page.</p>
```

<p class="text-center">This is a block of text that will be moved to the centre of the page.</p>

```Copy

<p class="text-right">This is a block of text that will be moved to the right of the page.</p>
```

<p class="text-right">This is a block of text that will be moved to the right of the page.</p>

### Links

Add a link is simple and should use the following code:

```Copy

<a href="https://seacrowbooks.com/">SeaCrow website.</a> 
```

In this code the a is an anchor for the link. The href is the site that the user will be sent to.

The link can be added to existing text:

```Copy
<p>This is a link to the <a href="https://seacrowbooks.com/">SeaCrow website.</a><p>
```

There is no need for any CSS class, since they are styled by the site CSS and, possibly, the branding CSS.

However, please note that the behaviour of this link is to send the user to a new page. If you want to keep them one the current page, but open a new tab in addition then use the following code that contains the target attribute:

```Copy

<p>This is a link to the <a href="https://seacrowbooks.com/" target="_blank">SeaCrow website.</a><p>
```

### Lists
There are two ways to present text as a list: ordered list and unordered list. 

Each list consists of two components, the list and the list item. 

The list tag can be either:

Unordered - \<ul>\</ul>
Ordered - \<ol>\</ol>

No matter which list you choice, the list item is always \<li>list item\</li>

#### Unordered List

```Copy 

<ul>
<li>Item one.</li>
<li>Item two</li>
<li>Item three</li>
</ul>
```

- Item one.
- Item two.
- Item three.

#### Ordered List

```Copy
<ol>
<li>Item one.</li>
<li>Item two</li>
<li>Item three</li>
</ol>
```

- Item one.
- Item two.
- Item three.

### Additional Formatting

Bootstrap gives us additional formatting options. 

#### Unstyled Lists

Bootstrap allows us to use the 'list-unstyled' class to remove formatting. [https://getbootstrap.com/docs/5.3/content/typography/](https://getbootstrap.com/docs/5.3/content/typography/)**

```Copy

<ul class="list-unstyled">
  <li>This is a list.</li>
  <li>It appears completely unstyled.</li>
  <li>Structurally, it's still a list.</li>
  <li>However, this style only applies to immediate child elements.</li>
  <li>Nested lists:
    <ul>
      <li>are unaffected by this style</li>
      <li>will still show a bullet</li>
      <li>and have appropriate left margin</li>
    </ul>
  </li>
  <li>This may still come in handy in some situations.</li>
</ul>
```

This is a list.
It appears completely unstyled.
Structurally, it's still a list.
However, this style only applies to immediate child elements.
Nested lists:
-  are unaffected by this style
- will still show a bullet
- and have appropriate left margin
This may still come in handy in some situations.

#### Inline List
You can use the 'list-inline' class for different formatting. Please note that the UL and LI tags require classes.

```Copy

<ul class="list-inline">
  <li class="list-inline-item">This is a list item.</li>
  <li class="list-inline-item">And another one.</li>
  <li class="list-inline-item">But they're displayed inline.</li>
</ul>
``````

This is a list item. And another one. But they're displayed inline.

## Blockquotes

A blockquote is used to indicate a quote or similar text. It should be used carefully but can have an impactful result. 

The quote is styled by the Seacrow site CSS and the theme CSS. 

```Copy

  <blockquote class="blockquote">

    <p>A well-known quote, contained in a blockquote element.</p>

  </blockquote>
```


> A well-known quote, contained in a blockquote element.

## Images

Special attention should be paid to placing images. It is essential they are placed with the correct HTML formatting. If not, they will not show or not position correctly. 

Please note: the quickest, and preferred, way to create the correct code is to the use the image generator in the site: [https://seacrowbooks.com/image_resources](https://seacrowbooks.com/image_resources) 

Click the link above and then go to the image page. Here you will find the code for the image which can be copy and pasted.

Here's an example:

```Copy

<img src="https://seacrowbooks.com/image_resources/romance-fiction/permanent_image" alt="two people kissing in front of lake" class="img-fluid post-show__media rounded mx-auto d-block" width="" height="">
```

<img src="https://seacrowbooks.com/blog/image_resources/steampunk-romance/permanent_image" alt="two people kissing in front of lake" class="img-fluid post-show__media rounded mx-auto d-block" width="700" height="400">

Find out more about the img tag: [https://www.w3schools.com/tags/tag_img.asp](https://www.w3schools.com/tags/tag_img.asp) 

Things to note:

- The src attribute is the way the browser knows what image to show. This is the full URL link to the image. Please use the link created by the image tool on the website. This allows the image to be changed and the link remain permanent. 
- The alt attribute serves two purposes. The first is to provide a description of the image for visually impaired users. The second is to provide some level of SEO information. Ideally the alt attribute should be descriptive but also include the post key word or phrase. 
- The 'img-fluid' class is used by bootstrap to resize the image on different platforms. The 'rounded' rounds the corner of the image and 'mx-auto d-block' centralises. 
- The 'post-show__media' class is used by the system CSS to add additional styling. 
- The width and height set the size of the image. These are displayed in pixels. As default they are left blank and the system/Bootstrap CSS will size the image. However, you may want some fine control, to do this, simply add the sizes. E.g. width="800" height="500".
    

```Copy

<img src="https://seacrowbooks.com/image_resources/romance-fiction/permanent_image" alt="two people kissing in front of lake" class="img-fluid post-show__media rounded mx-auto d-block" width="800" height="500">
```

<img src="https://seacrowbooks.com/image_resources/romance-fiction/permanent_image" alt="two people kissing in front of lake" class="img-fluid post-show__media rounded mx-auto d-block" width="800" height="500">

## Iframes

Iframes are little blocks of code that allow other code to be added via HTML. They are limited, very specific use cases, for us this will almost certainly be adding a YouTube video. Another case you may come across is to add a map.

```Copy

<video>

  <div class="ratio ratio-16x9 post-show__media">

    <iframe src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0" title="YouTube video" allowfullscreen></iframe>
  </div>

</video>
```

There are a few things to notice about this code:

- The \<video> tag is telling Google this is a video. It's called a media tag. You can find out more here. [https://www.w3schools.com/html/html5_video.asp](https://www.w3schools.com/html/html5_video.asp). The video tag can be given attributes (such as height and width) but these should be ignored.   
- The 'ratio' and 'ratio-16x9' classes come from Bootstrap and provide responsive sizing. The ratio size can be altered but do this with extreme caution. [https://getbootstrap.com/docs/5.3/helpers/ratio/](https://getbootstrap.com/docs/5.3/helpers/ratio/)
- The 'post-show__media' class is a system class and it used to add additional CSS styling. 
- The iframe is created by YouTube. Go to the video you want to embed and click the 'share' button. This will pop up a modal with options. Click the 'embed' option. Copy the iframe and use that in the post.

## Alerts

Alerts are used to create callouts in the body of the post. These are a Bootstrap element and need to include the correct classes. You can place anything you wish within the alert div class, though it works best with no tags if adding simple text with a link. 

```Copy

<div class="alert alert-info post-show__alert" role="alert">

  To discover more about Period piece romance, read <a href="https://seacrowbooks.com/blog/period-piece-romance">this extensive article</a>. 

</div>
```

Please note, that it is essential to include all the classes listed here. 

There is an option to alter the colour of the alert and you can find more information here: [https://getbootstrap.com/docs/5.3/components/alerts/#examples](https://getbootstrap.com/docs/5.3/components/alerts/#examples) However, you must understand that the system brand CSS alters the colour of the default colours, such as 'primary'. So it may need some experimentation.


> [!This is an alert]
> To discover more about Period piece romance, read <a href="https://seacrowbooks.com/blog/period-piece-romance">this extensive article</a>. 

## Table of Contents
The table of contents is an important part of most posts and its created using a mixture of structural and brand CSS, together with Bootstrap classes. It is essential that these instructions are followed closely since it's easy to break the table of contents. 

There are two parts:

- Part 1: The opening section that appears at the start of the post. 
- Part 2: The way in which the headers are formatted.

### Part 1
```Copy

<div class="table-of-contents card bg-light" id="toc">
 <p class="card-header table-of-contents__title">Table of Contents</p>
  <div class="card-body">
    <ul>
      <li class=”table-of-contents__link”><a href="#parent-link">Parent Link</a></li>
      <li class="table-of-contents__link-child"><a href="#child-link">Child Link</a></li>
    </ul>
  </div>
</div>
```

- The card, which is styled by Bootstrap. 
- The card header, which is styled by Bootstrap and CSS.
- The UL list. 
- The li elements. It's possible to have the primary and secondary, child element, though this child is is not required. 

### Part 2

```Copy

  <h2 class="post-show__sub-title" id="parent-link">Parent Link</h2>
  <h3 class="post-show__sub-title" id="child-link">Child Link</h3>
```

- The code above is for parent and child links. Note that the child link (H2) is not required.

## Frequently Asked Questions

FAQ sections are formatted via bootstrap and the theme CSS. They are also presented in a way that includes structured, semantic, data. It is important the format is followed closely.

More information here: [https://developers.google.com/search/docs/advanced/structured-data/faqpage](https://developers.google.com/search/docs/advanced/structured-data/faqpage)

```html

<section id="faq" class="faq">
<div itemscope itemtype="https://schema.org/FAQPage" class="faq">

<h2 class="faq__title" id="faq">Frequently Asked Questions</h2>
<p class="faq__description">Below are some frequently asked questions that will provide you with more information.</p>

	<div itemscope itemprop="mainEntity" itemtype="https://schema.org/Question" class="faq__block">
	<h3 itemprop="name" class="faq__question">Question here</h3>
	<div itemscope itemprop="acceptedAnswer" itemtype="https://schema.org/Answer">
  	<div itemprop="text" class="faq__answer">
    	<p>Answer here</p>
  	</div>
	</div>
  </div>
 
 	</div>
</section>

```
## Semantic Elements

Semantic elements are an important part of any blog post. It is suggested you read the following if you intend to use these elements: https://www.w3schools.com/html/html5_semantic_elements.asp

Utilizing semantic HTML elements in your blog post enhances readability and accessibility. Here's how to use them:

\<article> Wraps the entire blog post to indicate a self-contained composition.
   
```Copy

   <article>
     <!-- Your blog post content -->
   </article>
```

\<section> Groups thematic content, making your post organized.

```Copy

<section>
  <!-- A thematic part of your post, like a subsection -->
</section>
```

\<aside> Represents content related to the main theme but can be separate, like a sidebar.

```Copy

<aside>
  <!-- Sidebar content -->
</aside>
```

\<figure> and \<figcaption> for encapsulating media and their captions.

```Copy

<figure>
  <img src="image.jpg" alt="Description">
  <figcaption>Description of image</figcaption>
</figure>
```
\<time> represents a specific period of time.

```Copy

<time datetime="2023-10-24">October 24, 2023</time>
```

These elements help communicate the structure of your post to both readers and browsers, enhancing the overall accessibility and clarity of your content.