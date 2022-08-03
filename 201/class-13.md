## Class-13 Reading Notes  
<p>The use of local storage done properly can optimize web app performance.</p>

### Local Storage and How To Use It On Websites

1. Why would a developer use local storage for a web application?
    * Local storage of web service data, i.e. caching data locally when there are latency issues; among other things, helps if an API fails, as you still have information to display.
    * Maintaining the state of an interface, e.g. storing an entire HTML or maintaining an object with the state of all your widgets.
2. What information should not be stored in local storage?
    * For security reasons, personal information and password should be exempted.
3. Local storage can store what type of data? How would you convert it to that type before storing?
    * Data is only stored in strings, but workarounds such as JSON.stringify() and JSON.parse() methods solve this issue.


## Things I want to know more about

1. I am especially interested in understanding the security issues around local storage -- I know this is an area that is ever-changing, and would want to know how to keep abreast of the latest, e.g. the modern equivalents of the *evercookie* referenced in the article.