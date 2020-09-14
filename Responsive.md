When you are done with your non-responsive website, the first thing to do is to paste this lines in the <head>

<p><code><meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no"></code></p>
<p><code><meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"></code></p>
<p><code>"<meta name="HandheldFriendly" content="true""</code></p>
  
It’s now time to add some media queries. The first have a maximum width of 1060px and is optimized for tablet landscape display. #primary occupies 67% of its parent container, and #secondary 30%, plus a 3% left margin.

The second size is designed for tablet portrait and smaller sizes. Due to the small sizes of smartphones screens, I decided to give #primary a 100% width. #secondary also have a 100% width, and will be displayed below #primary.


/* Tablet Landscape */
@media screen and (max-width: 1060px) {
    #primary { width:67%; }
    #secondary { width:30%; margin-left:3%;}  
}
/* Tabled Portrait */
@media screen and (max-width: 768px) {
    #primary { width:100%; }
    #secondary { width:100%; margin:0; border:none; }
}



<a href="https://www.codecademy.com/">Codecademy</a>

<a href="https://www.freecodecamp.org/">freeCodeCamp</a>

<a href="https://www.udemy.com/">Udemy</a>
