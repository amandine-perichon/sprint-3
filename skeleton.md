What happens to the layout when you resize the screen to less than 550 px. How do you think that works? 

The Skeleton demo website is responsive, the layout changes depending on the size of the screen. The layout adapts to fit the page elements on in a smaller screen, for instance by going from 2 or 3 columns to 1 column.

There are two CSS files applied to the Skeleton website:
- the Skeleton CSS
- a custom CSS for the website

Both are linked in the HTML:

  &lt;link rel="stylesheet" href="../../dist/css/skeleton.css"&gt;

  &lt;link rel="stylesheet" href="css/custom.css"&gt;

The custom CSS link comes after the Skeleton link, which means that, if both files contain the same CSS rule, the custom CSS will be applied (instead of the Skeleton CSS).

Both CSS use media queries to specify CSS rules that will apply for screens larger than 550px (as well as 750px and 1000px). 
When you resize the screen to less than 550px, we are in conditions where the CSS rules included in the media queries do not apply, hence the basic CSS rules apply (those not included in the media queries). In other words, the CSS is written in a mobile first approach: CSS rules apply to mobile, unless they are included in the media queries.