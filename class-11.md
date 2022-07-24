## Class-11 Reading Notes  
<p>The domain I have been most familiar with the past few years from the business side is the news publishing space, and to put it mildly, the players in that space rely heavily on video, and increasingly audio. This seems like a super relevant topic, since this type of content receives massive engagement.</p>

### Video and Audio Content

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s.
    * In the early days, bandwidth constraints preempted video; when bandwidth increased more broadly, the only solutions were proprietary like Flash and Silverlight (both of which had issues, and importantly security was one of them); eventually HTML5  added the necessary features, with <video\> and <audio\> elements and accompanying JS APIS to access and control them. 
2. Describe the use of the src and controls attributes in the <video\> element.
    * Src is the same as for the image element -- simply provides a file path to the source video file.
    * Controls refers to basic video player functionality like stop and play - controls utilizes the browsers built-in functionality; optionally can do your own interface via APIs with JS.
3. Why is it important to have fallback content inside the <video\> element?
    * This is the equivalent of alt in image elements -- if the browser doesn't support the format of the video being served, the user will get a message and typically a direct link to the video.
4. Write a very short story where <audio\> and <video\> are characters.
    * <audio\> and <video\> get in an argument over whether the sound of music or the glory of video is the superior media, but they are interrupted by the seemingly lowly p tag <p\>, who admonishes them both with, "To <p\> or not to <p\>, that is the question."  Just as <audio\> and <video\> joined forces to attack <p\>, a newbie developer lost them all with a git gaffe.  So in the end they all paid the highest price...and were known to posterity for eternity as the *price tags*.

### A Complete Guide To Grid

1. How does Grid layout differ from Flex?
    * The basic difference between CSS Grid Layout and CSS Flexbox Layout is that flexbox was designed for layout in one dimension - either a row or a column. Grid was designed for two-dimensional layout - rows and columns at the same time.
2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.
    * Grid container: the parent element on which 'display: grid' is applied.
    * Grid item: the children of the grid container.
    * Grid line: the vertical (columnar) and horizontal (row) grid lines that provide the structure of the grid.

### Responsive Images

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?
    * There is also the issue of serving overly large images to mobile screens and unnecessarily taking up excess bandwidth.
2. Define the following <img\> attributes srcset and sizes. Write an example of how they are used.
    * srcset defines the images available to the browser to use, and their respective sizes.
    * Sizes defines media conditions, usually screen size, and effectively is an if statement whereby different sized images are chosen depending on screen size.
3. How is srcset more helpful for responsive images than CSS or JavaScript?
    * Because browser download larger images files first so to reduce download times overall, and the larger files would already be in the process of downloading by the time the CSS and JS code ran, i.e. the horse has already left the stable.

## Things I want to know more about

1. I look forward to playing with these in lab, and am also interested in learning about best practices in how to link to OVPs like YouTube.