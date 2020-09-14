<b>•HOW TO START</b>

When you are done with your non-responsive website, the first thing to do is to paste this lines in the HEAD

     <meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
     <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
     <meta name="HandheldFriendly" content="true">
  
It’s now time to add some media queries. The first have a maximum width of 1060px and is optimized for tablet landscape display. #primary occupies 67% of its parent container, and #secondary 30%, plus a 3% left margin. The second size is designed for tablet portrait and smaller sizes. Due to the small sizes of smartphones screens, I decided to give #primary a 100% width. #secondary also have a 100% width, and will be displayed below #primary.

Tablet:

     @media screen and (max-width: 1060px) {
     #primary { width:67%; }
     #secondary { width:30%; margin-left:3%;}  
     }

Portrait:

    @media screen and (max-width: 768px) {
    #primary { width:100%; }
    #secondary { width:100%; margin:0; border:none; }
    }

<b>•IMAGES</b>

Please note that the max-width directive is not recognized by older browsers such as IE6. In order to work, this code snippet have to be inserted into your CSS stylesheet.

     img { max-width: 100%; }
     
     
     @media (min-device-width:600px) {
    img[data-src-600px] {
        content: attr(data-src-600px, url);
    }
     }
     @media (min-device-width:800px) {
    img[data-src-800px] {
        content: attr(data-src-800px, url);
    }
     }
     
     
•<b>VIDEOS</b>

HTML
     
     <div class="video-container">
     <iframe src="http://player.vimeo.com/video/6284199?title=0&byline=0&portrait=0" width="800" height="450" frameborder="0"></iframe>
     </div>

CSS

     .video-container {
     position: relative;
     padding-bottom: 56.25%;
     padding-top: 30px;
     height: 0;
     overflow: hidden;
     }
     .video-container iframe,  
     .video-container object,  
     .video-container embed {
     position: absolute;
     top: 0;
     left: 0;
     width: 100%;
     height: 100%;
     }

•<b>TYPOGRAPHY</b>

The CSS3 specification included a new unit named rems. They work almost identically to the em unit, but are relative to the html element, which make them a lot easier to use than ems. As rems are relative to the html element, don’t forget to reset html font size:

     html { font-size:100%; }
     
Once done, you can define responsive font sizes as shown below:

     @media (min-width: 640px) { body {font-size:1rem;} } 
     @media (min-width:960px) { body {font-size:1.2rem;} } 
     @media (min-width:1100px) { body {font-size:1.5rem;} }

•<b>TEST IT</b>

<p>You can check how responsive your website is <a href="http://mattkersley.com/responsive/">Here</a></p>
