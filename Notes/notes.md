# The Road So Far...


## Intermediate HTML and CSS 
   **What I learned:**

1. Learned about the Emmet plugin for VS Code. 
It utilizes shortcuts to generate boilerplate HTML and automatically create the start/end tags for many HTML elements. 
Some useful abbreviations are: 
    "!" generate the DOCTYPE Declaration as well as, head and body tags ->

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8" />
            <title>Document</title>
        </head>
        <body> 
        </body>
        </html>

    Child: ">" to embed elements within each other and automatically create their start and end tags -> 

        nav>ul>li
            <nav>
                <ul>
                    <li></li>
                </ul>
            </nav> 


2. SVG, or Scalable Vector Graphics is a scalable image format, that will easily scale to any size and retain their quality without increasing their filesize. They’re also very useful if you need to create or modify your images programmatically, because you can change their properties through CSS and JavaScript.
    SVGs are often used for:
- Icons
- Graphs/Charts
- Large, simple images
- Patterned backgrounds
- Applying effects to other elements via SVG filters

### Why is SVG Useful:
- SVG are defined using XML(Extensible Markup Language), which means that it's human readable unlike JPEG or other traditional raster graphics standards/ binary file formats. An example of SVG in XML would look like this:  

        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
            <rect x=0 y=0 width=100 height=50 />
            <circle class="svg-circle" cx="50" cy="50" r="10"/>
        </svg>
    

- The second benefit of XML is that it’s designed to be interoperable with HTML, which means you can put the above code directly in an HTML file, without any changes, and it should display the image. And because these can become elements in the DOM just like HTML elements, you can target them with CSS and create them using the [Element WebAPI](https://developer.mozilla.org/en-US/docs/Web/API/Element).

### SVG Drawbacks: 
- SVGs main strengths are for simple images, but because every single detail of the image needs to be written out as XML, they are inefficient at storing complex images. If your image is supposed to be photo-realistic, has fine detail, or texture (“grunge textures” are a great example), then SVGs are the wrong tool for the job. 

### Anatomy of an SVG
1. xmlns - stands for “XML NameSpace”. This specifies what dialect of XML you’re using. In our case, that dialect is the SVG language spec. Without it, some browsers will not render your image or will render it incorrectly.

2. viewBox - defines the bounds of your SVG. When you have to define the positions of different points of the elements in your SVG, this is what that’s referencing. It also defines the aspect ratio and the origin of your SVG.

3. class, id - these attributes function just like they do in HTML. Using these in SVGs allows you to easily target an element via CSS or JavaScript, or to reuse an element via the [use element](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/use).

4. Elements such as `<circle>, <rect>, <path>, and <text>` are defined by the SVG namespace. These are our basic building-blocks. Although you can make extremely complex images with SVG, they are mostly created with just a dozen or so of these basic elements. You can see a complete list of SVG elements [here](https://developer.mozilla.org/en-US/docs/Web/SVG/Element).

5. SVG attributes, such as fill and stroke, can be changed in your [CSS](https://css-tricks.com/svg-properties-and-css/).


### Embedding SVGs
There are two main approaches when deciding how to actually place the SVG in your document: linked and inline.

Linking:
- Linking SVGs works basically the same way as linking any other image. You can use an HTML image element such as `<img>`, or link it in your CSS using background-image: url(./my-image.svg). They will still scale properly, but the contents of the SVG will not be accessible from the webpage.

Inline:
- You can inline your SVGs by pasting their contents directly into your webpage’s code, rather than linking to it as an image. It will still render correctly, but the SVG’s properties will be visible to your code, which will allow you to alter the image dynamically via CSS or JavaScript.

- Inlining SVGs allows you to unlock their full potential, but it also comes with some serious drawbacks: it makes your code harder to read, makes your page less cacheable, and if it’s a large SVG it might delay the rest of your HTML from loading.

- Some of the drawbacks of inlining SVG code can be avoided with a front-end JavaScript library like React.



---
## JavaScript 



---
## Advanced HTML and CSS 


---
## NodeJS
