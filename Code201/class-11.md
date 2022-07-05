# Audio, Video, Images

## Video and Audio Content
https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content


The <video> HTML element embeds a media player which supports video playback into the document. You can use <video> for audio content as well, but the <audio> element may provide a more appropriate user experience.

<video controls width="250">

    <source src="/media/cc0-videos/flower.webm"
            type="video/webm">

    <source src="/media/cc0-videos/flower.mp4"
            type="video/mp4">

    Sorry, your browser doesn't support embedded videos.
</video>



The <audio> HTML element is used to embed sound content in documents. It may contain one or more audio sources, represented using the src attribute or the <source> element: the browser will choose the most suitable one. It can also be the destination for streamed media, using a MediaStream.

HTML
<figure>
    <figcaption>Listen to the T-Rex:</figcaption>
    <audio
        controls
        src="/media/cc0-audio/t-rex-roar.mp3">
            Your browser does not support the
            <code>audio</code> element.
    </audio>
</figure>

CSS
figure {
    margin: 0;
}



1 Explain how the ability to use video and audio on the web has evolved since the early 2000s.

Web developers have wanted to use video and audio on the Web for a long time, ever since the early 2000s when we started to have bandwidth fast enough to support any kind of video (video files are much larger than text or even images.) In the early days, native web technologies such as HTML didn't have the ability to embed video and audio on the Web, so proprietary (or plugin-based) technologies like Flash — and later, Silverlight (both of which are now obsolete) — became popular for handling such content.

Fortunately, a few years later the HTML5 specification had such features added, with the <video> and <audio> elements, and some shiny new JavaScript APIs for controlling them.


2. Describe the use of the src and controls attributes in the <video> element.

src    https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video#attr-src
In the same way as for the <img> element, the src (source) attribute contains a path to the video you want to embed. It works in exactly the same way.

<video src="rabbit320.webm" controls>
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.webm">link to the video</a> instead.</p>
</video>


controls  https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video#attr-controls

Users must be able to control video and audio playback (it's especially critical for people who have epilepsy.) You must either use the controls attribute to include the browser's own control interface, or build your interface using the appropriate JavaScript API. At a minimum, the interface must include a way to start and stop the media, and to adjust the volume.


3. Why is it important to have fallback content inside the <video> element?

The paragraph inside the <video> tags
This is called fallback content — this will be displayed if the browser accessing the page doesn't support the <video> element, allowing us to provide a fallback for older browsers. This can be anything you like; in this case, we've provided a direct link to the video file, so the user can at least access it some way regardless of what browser they are using.


4. Write a very short story where <audio> and <video> are characters.

Here you have paternal twins, thier names are Audio and Video. They look realatively the same but have a couple of differnt attributes. Poor little Audio isn't much of a looker but has a smaller size, gets along well with everyone, and has a beautiful voice. Video on the other hand got all the looks, even if her size is quite larger. But her temperment is all based on who she's playing with. She has more conflicts than her sister, and is sometimes misunderstood.


## A Complete Guide To Grid
https://css-tricks.com/snippets/css/complete-guide-grid/


Table of contents
Introduction
Basics & Browser Support
Important Terminology
Grid Properties
Special Units & Functions
Fluid Columns Snippet
Animation

1. How does Grid layout differ from Flex?

CSS Grid Layout (aka “Grid” or “CSS Grid”), is a two-dimensional grid-based layout system that, compared to any web layout system of the past, completely changes the way we design user interfaces.

 CSS has always been used to layout our web pages, but it’s never done a very good job of it. First, we used tables, then floats, positioning and inline-block, but all of these methods were essentially hacks and left out a lot of important functionality (vertical centering, for instance). 
 
 Flexbox is also a very great layout tool, but its one-directional flow has different use cases — and they actually work together quite well! Grid is the very first CSS module created specifically to solve the layout problems we’ve all been hacking our way around for as long as we’ve been making websites.



2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.

Grid Container https://css-tricks.com/snippets/css/complete-guide-grid/#:~:text=many%20of%20them.-,Grid%20Container,-The%20element%20on

The element on which display: grid is applied. It’s the direct parent of all the grid items. In this example container is the grid container.

Grid Item https://css-tricks.com/snippets/css/complete-guide-grid/#:~:text=1%20and%203.-,Grid%20Item,-The%20children%20(i

The children (i.e. direct descendants) of the grid container. Here the item elements are grid items, but sub-item isn’t.

Grid Line  https://css-tricks.com/snippets/css/complete-guide-grid/#aa-grid-item:~:text=%3C/div%3E-,Grid%20Line,-The%20dividing%20lines

The dividing lines that make up the structure of the grid. They can be either vertical (“column grid lines”) or horizontal (“row grid lines”) and reside on either side of a row or column.



## Responsive Images
https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images


1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?

The concept of responsive images — images that work well on devices with widely differing screen sizes, resolutions, and other such features — and look at what tools HTML provides to help implement them.


2. Define the following <img> attributes srcset and sizes. Write an example of how they are used.

Two image attributes srcset and sizes — to provide several additional source images along with hints to help the browser pick the right one.

<img srcset="elva-fairy-480w.jpg 480w,
             elva-fairy-800w.jpg 800w"
     sizes="(max-width: 600px) 480px,
            800px"
     src="elva-fairy-800w.jpg"
     alt="Elva dressed as a fairy">


srcset defines the set of images we will allow the browser to choose between, and what size each image is. Each set of image information is separated from the previous one by a comma.

1. An image filename (elva-fairy-480w.jpg)
2. A space
3. The image's intrinsic width in pixels (480w) — note that this uses the w unit, not px as you might expect. An image's intrinsic size is its real size, which can be found by inspecting the image file on your computer (for example, on a Mac you can select the image in Finder and press Cmd + I to bring up the info screen).


3. How is srcset more helpful for responsive images than CSS or JavaScript?

When the browser starts to load a page, it starts to download (preload) any images before the main parser has started to load and interpret the page's CSS and JavaScript. That mechanism is useful in general for reducing page load times, but it is not helpful for responsive images — hence the need to implement solutions like srcset. For example, you couldn't load the <img> element, then detect the viewport width with JavaScript, and then dynamically change the source image to a smaller one if desired. By then, the original image would already have been loaded, and you would load the small image as well, which is even worse in responsive image terms.



# Bookmark and Review

Images in HTML   https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML

Other Embedding Technologies   https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies


## Things I want to know more about

 WebP https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#webp_image
 
 AVIF  https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#avif_image

 

