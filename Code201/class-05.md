# HTML Media

What is a real world use case for the alt attribute being used in a website?

The user is visually impaired, and is using a screen reader to read the web out to them. In fact, having alt text available to describe images is useful to most users.
As described above, the spelling of the file or path name might be wrong.
The browser doesn't support the image type. Some people still use text-only browsers, such as Lynx, which displays the alt text of images.
You may want to provide text for search engines to utilize; for example, search engines can match alt text with search queries.
Users have turned off images to reduce data transfer volume and distractions. This is especially common on mobile phones, and in countries where bandwidth is limited or expensive.


How can you improve accessibility of images in an HTML document?

Add a blank alt="" in HTML. If the image isn't part of the content, a screen reader shouldn't waste time reading it.

Use the HTML5 <figure> and <figcaption> elements. These are created for exactly this purpose: to provide a semantic container for figures, and to clearly link the figure to the caption. 

<figure>
  <img src="images/dinosaur.jpg"
       alt="The head and torso of a dinosaur skeleton;
            it has a large head with long sharp teeth"
       width="400"
       height="341">

  <figcaption>A T-Rex on display in the Manchester University Museum.</figcaption>
</figure>


Provide an example of when the figure element would be useful in an HTML document.

A figure doesn't have to be an image. It is an independent unit of content that:

Expresses your meaning in a compact, easy-to-grasp way.
Could go in several places in the page's linear flow.
Provides essential information supporting the main text.
A figure could be several images, a code snippet, audio, video, equations, a table, or something else.

Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.

GIF is a good choice for simple images and animations, although converting full color images to GIF can result in unsatisfactory dithering.

SVG is an XML-based vector graphics format that specifies the contents of an image as a set of drawing commands that create shapes, lines, apply colors, filters, and so forth. SVG files are ideal for diagrams, icons, and other images which can be accurately drawn at any size. As such, SVG is popular for user interface elements in modern Web design.

SVG files are text files containing source code that, when interpreted, draws the desired image. For instance, this example defines an drawing area with initial size 100 by 100 units, containing a line drawn diagonally through the box:

<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <line x1="0" y1="80" x2="100" y2="20" stroke="black" />
</svg>

SVG can be used in web content in two ways:

You can directly write the <svg> element within the HTML, containing SVG elements to draw the image.
You can display an SVG image anywhere you can use any of the other image types, including with the <img> and <picture> elements, the background-image CSS property, and so forth.
SVG is an ideal choice for images which can be represented using a series of drawing commands, especially if the size at which the image will be rendered is unknown or may vary, since SVG will smoothly scale to the desired size. It's not generally useful for strictly bitmap or photographic images, although it is possible to include bitmap images within an SVG.


What image type would you use to display a screenshot on your website and why?

Best choice-Lossless WebP or PNG; JPEG if compression artifacts aren't a concern.
Fallback PNG or JPEG; GIF for screenshots with low color counts

# Learn CSS

Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.

At a fundamental level, the color property defines the foreground color of an HTML element's content and the background-color property defines the element's background color. These can be used on just about any element.


Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?
What should you consider when choosing fonts for an HTML document?

Background color, borders, text box variation colors, for the font changing font family, color, bolding text are some of the examples.


What do font-size, font-weight, and font-style do to HTML text elements?



Describe two ways you could add spacing around the characters displayed in an h1 element.

The letter-spacing and word-spacing properties allow you to set the spacing between letters and words in your text. You won't use these very often, but might find a use for them to obtain a specific look, or to improve the legibility of a particularly dense font. They can take most length and size units.