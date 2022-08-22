---
title: About
layout: page
permalink: /about.html
# Edit the markdown on in this file to describe your collection
---

{% include about/jumbotron.html %}

# About Global South Postcards.
Global South Postcards is a gallery of online postcard images from Korea and Mexico during the initial decades of picture postcard production. The gallery is meant as a comparative resource from two widely separated countries that nevertheless experienced the colonizing gaze of postcard producers and consumers in similar ways. Both were situated as incipiently modern, promising in their cultural riches and histories, yet othered and neutered, as it were, by the colonizing processes. These images show the consistency of the colonizing visual discourses to which countries in the global south were subject, regardless of the specific histories and conditions of each country.

Several developments of a technical and diplomatic nature combined to create the first postcard boom shortly after the turn of the twentieth century. On the technological front, photography and photomechanical reproduction had developed to the point where it was economically feasible to print high quality photographs on card stock, and sell them cheaply. On the diplomatic front, the establishment of an international postal agreement allowed for the mailing of postcards across international borders, and beginning in 1900 (in Korea and Mexico), postcards with printed images were allowed (contrasting with the relatively boring cards made prior to that by national postal services, which bore no image other than the stamp). These changes resulted in an immediate globalized media phenomenon, with collectors feverishly exchanging postcards from all parts of the globe, and small and large photography and printing companies producing millions of cards.


# About GitHub Collection Builder.
This site is generated using `collectionbuilder-gh`, a project to generate a free and simple digital collection using [GitHub Pages](https://pages.github.com/) from: 

- a CSV of collection metadata
- a folder of JPEG images or PDF documents

`collectionbuilder-gh` is intended as a simple template for hands-on teaching about digital libraries.
It can be used in a workshop setting to take participants through digitization and metadata creation, to having a live collection site hosted on GitHub.

# Demo about features

You can use Liquid includes to add Bootstrap features to Markdown pages in your collection site. 
See the includes in `_includes/feature/` directory.

## Figure 

To add an image from the collection into an interpretive page, use the `item-figure.html` include. 

The base include requires one option, an `objectid` of an item from the collection:

`{% raw %}{% include feature/item-figure.html objectid="postcards_test_469" %}{% endraw %}`

This include will become: 

{% include feature/item-figure.html objectid="postcards_test_469" %}

Three further options allow you to style it. 

- `width`: 25, 50, 75, or 100
- `float`: left or right
- `caption`: By default the include automatically adds the item title as the caption. If you would like to override that, use `caption=false` for none, or `caption="Example caption"` to manually create one.

For example: 

`{% raw %}{% include feature/item-figure.html objectid="postcards_test_469" width="50" float="left" caption="Example 50% width and floating left" %}{% endraw %}`

Becomes: 

{% include feature/item-figure.html objectid="postcards_test_469" width="50" float="left" caption="Example 50% width and floating left" %}

You will probably want to "clear" the float at some point in your text. 
Add `<div class="clearfix"></div>` on it's own line to do so. 
The clearfix div is added below this paragraph, thus the next section will NOT wrap around the floating figure and will start below.

<div class="clearfix"></div>

## Alert 

[Bootstrap Alert](https://getbootstrap.com/docs/4.4/components/alerts/) is a quick way to set some text apart. 
The include has three options: 
`text` (what it says, can be in Markdown), `color` (a Bootstrap color), `align` (the text alignment).

For example: 

`{% raw %}{% include feature/alert.md text="Example alert text" color="success" align="center" %}{% endraw %}`

Becomes:

{% include feature/alert.md text="Example alert text" color="success" align="center" %}

## Card

[Bootstrap Card](https://getbootstrap.com/docs/4.4/components/card/) in another option to breakup long text into smaller organized units. 
The options allow you to set up all the Card elements. 

- "text" = main card text, can use markdown formatting. Use a Liquid capture to add more complex content.
- "header" = card header text (in bar above card content)
- "title" = card title text inside card content area
- "objectid" = the given object (photo or youtube) will create a card cap image
- "width" will use Bootstrap sizing to set the % size, choose from "25", "50", "75", or "100"
- "float" will use Bootstrap float utility to add float, choose from "left" or "right"

For example:

```{% raw %}
{% capture exampletext %}
An example card with:

- header
- title
- text

{% endcapture %}
{% include feature/card.md text=exampletext header="Example header" title="Title example" %}{% endraw %}
```

{% capture exampletext %}
An example card with:

- header
- title
- text

Becomes: 

{% endcapture %}
{% include feature/card.md text=exampletext header="Example header" title="Title example" %}

## Modal

[Bootstrap Modal](https://getbootstrap.com/docs/4.4/components/modal/) is a popup text feature. 
Options: 

- "button" = text of button to trigger modal
- "color" = color of modal button (primary, secondary, success, danger, warning, info, light, dark)
- "title" = header text for modal pop up
- "text" = body text for modal pop up, can use Markdown

This:

`{% raw %}{% include feature/modal.md button="Example Modal" color="success" title="Modal title" text="A bit of text in the modal" %}{% endraw %}`

Produces: 

{% include feature/modal.md button="Example Modal" color="success" title="Modal title" text="A bit of text in the modal" %}

## timelinejs.html 

Add a auto generated TimelineJS feature:

`{% raw %}{% include feature/timelinejs.html %}{% endraw %}`

Adds: 

{% include feature/timelinejs.html %}
