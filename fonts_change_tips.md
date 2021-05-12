## How to change the Font of your personal website
Many times it is required to change the font of our websites to make it more attractive. So this is a document that will expaline one of the easiest methods.
Before going to the shortcut method, you can go little deeper about web fonts [here](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Web_fonts).

#### So, the shortcut - most of the time I follow this method,
1. Google provides everything :-) go to [Google fonts](https://fonts.google.com)
2. Click on any font you liked.
3. Now it provides different verities of same fonts. Click on Select this style
4. Now a side bar will open, Select link option available under Use on the web section.
5. Copy the code  and paste it in you index.html just below the `<title></title>`
6. Open your style file(`style.css` (or other)) and paste the code given under *CSS rules to specify families*  
Note: If you want a font for your entire website,
```
body { font-family: 'Roboto', sans-serif;}
```
If you want a font just for a class
```
.class-name { font-family: 'Roboto', sans-serif; }
```
7. Done!  


This is one of the simplest method to change the font of our website. The font is actually saved on the google server. So there will be some time delay to load the font depends upon the internet speed. For faster loading of font, you needed to download to your folder and link to our webpage.
