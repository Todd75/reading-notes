# Course 201 Class Five "Images, Color, Text"

In order to put a simple image on a web page, we use the `<img>` element. This is a void element (meaning, it cannot have any child content and cannot have an end tag) that requires two attributes to be useful: src and alt. The src attribute contains a URL pointing to the image you want to embed in the page. As with thehref attribute for `<a>` elements, the src attribute can be a relative URL or an absolute URL. Without a src attribute, an img element has no image to load.

## Alternative text

The next attribute we'll look at is alt. Its value is supposed to be a textual description of the image, for use in situations where the image cannot be seen/displayed or takes a long time to render because of a slow internet connection.

So, why would you ever see or need alt text? It can come in handy for a number of reasons:

- The user is visually impaired, and is using a screen reader to read the web out to them. In fact, having alt text available to describe images is useful to most users.
- As described above, the spelling of the file or path name might be wrong.
- The browser doesn't support the image type. Some people still use text-only browsers, such as Lynx, which displays the alt text of images.
- You may want to provide text for search engines to utilize; for example, search engines can match alt text with search queries.
- Users have turned off images to reduce data transfer volume and distractions. This is especially common on mobile phones, and in countries where bandwidth is limited or expensive.

What exactly should you write inside your alt attribute? It depends on why the image is there in the first place. In other words, what you lose if your image doesn't show up:

- Decoration. You should use CSS background images for decorative images, but if you must use HTML, add a blank alt="". If the image isn't part of the content, a screen reader shouldn't waste time reading it.
- Content. If your image provides significant information, provide the same information in a brief alt text – or even better, in the main text which everybody can see. Don't write redundant alt text. How annoying would it be for a sighted user if all paragraphs were written twice in the main content? If the image is described adequately by the main text body, you can just use alt="".
- Link. If you put an image inside `<a>` tags, to turn an image into a link, you still must provide accessible link text. In such cases you may, either, write it inside the same `<a>` element, or inside the image's alt attribute – whichever works best in your case.
- Text. You should not put your text into images. If your main heading needs a drop shadow, for example, use CSS for that rather than putting the text into an image. However, If you really can't avoid doing this, you should supply the text inside the alt attribute.

## Width and height

Use the width and height attributes to specify the width and height of your image. You can find your image's width and height in a number of ways.

**If you need to alter an image's size, you should use CSS instead of HTML.**

## Image titles

As with links, you can also add title attributes to images, to provide further supporting information if needed.

## CSS background images

The CSS background-image property, and the other background-* properties, are used to control background image placement.

    p {
      background-image: url("images/anythingyouwant.jpg");
    }

The resulting embedded image is arguably easier to position and control than HTML images. So why bother with HTML images? As hinted to above, CSS background images are for decoration only. If you just want to add something pretty to your page to enhance the visuals, this is fine. Though, such images have no semantic meaning at all. They can't have any text equivalents, are invisible to screen readers, and so on. This is where HTML images shine!

Summing up: if an image has meaning, in terms of your content, you should use an HTML image. If an image is purely decoration, you should use CSS background images.

### Questions

1. What is a real world use case for the alt attribute being used in a website?

The alt attribute will help search engines find your photod by their description.

2. How can you improve accessibility of images in an HTML document?

By setting height and width sizes so the image appears faster on webpages and it also provides a size placeholder on pages.

3. Provide an example of when the figure element would be useful in an HTML document.

when you want to provide a caption for a picture.

4. Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.

A GIF would be used to put 5 cute puppy pictures in a row and shuffle through them whereas a svg. may be used to show how to complete a project with step by step overlays that show the steps until the project is completed by overlaying the steps on top of each other.

5. What image type would you use to display a screenshot on your website and why?

I would use a PNG format to keep lossless format over JPG you could also use WebP.

## Things that can have color

At the element level, everything in HTML can have color applied to it. Instead, let's look at things in terms of the kinds of things that are drawn in the elements, such as text and borders and so forth. For each, we'll see a list of the CSS properties that apply color to them.

### Text

- color
The color to use when drawing the text and any text decorations (such as the addition of under- or overlines, strike-through lines, and so forth.

- background-color
The text's background color.

- text-shadow
Configures a shadow effect to apply to text. Among the options for the shadow is the shadow's base color (which is then blurred and blended with the background based on the other parameters). See Text drop shadows in Fundamental text and font styling to learn more.

- text-decoration-color
By default, text decorations (such as underlines, strikethroughs, etc.) use the color property as their colors. However, you can override that behavior and use a different color for them with the text-decoration-color property.

- text-emphasis-color
The color to use when drawing emphasis symbols adjacent to each character in the text. This is used primarily when drawing text for East Asian languages.

- caret-color
The color to use when drawing the caret (sometimes referred to as the text input cursor) within the element. This is only useful in elements that are editable, such as `<input>` and `<textarea>` or elements whose HTML contenteditable attribute is set.

### Boxes

Every element is a box with some sort of content, and has a background and a border in addition to whatever contents the box may have.

` Borders
See Below

- background-color
The background color to use in areas of the element that have no foreground content.

- column-rule-color
The color to use when drawing the line separating columns of text.

- outline-color
The color to use when drawing an outline around the outside of the element. This outline is different from the border in that it doesn't get space set aside for it in the document (so it may overlap other content). It's generally used as a focus indicator, to show which element will receive input events.

### Borders

Any element can have a border drawn around it. A basic element border is a line drawn around the edges of the element's content. See Box properties in The box model to learn about the relationship between elements and their borders, and the article Styling borders using CSS to learn more about applying styles to borders.

You can use the border shorthand property, which lets you configure everything about the border in one shot (including non-color features of borders, such as its width, style (solid, dashed, etc.), and so forth.

- border-color
Specifies a single color to use for every side of the element's border.

- border-left-color, border-right-color, border-top-color, and border-bottom-color
Lets you set the color of the corresponding side of the element's border.

- border-block-start-color and border-block-end-color
With these, you can set the color used to draw the borders which are closest to the start and end of the block the border surrounds. In a left-to-right writing mode (such as the way English is written), the block start border is the top edge and the block end is the bottom. This differs from the inline start and end, which are the left and right edges (corresponding to where each line of text in the box begins and ends).

- border-inline-start-color and border-inline-end-color
These let you color the edges of the border closest to the beginning and the end of the start of lines of text within the box. Which side this is will vary depending on the writing-mode, direction, and text-orientation properties, which are typically (but not always) used to adjust text directionality based on the language being displayed. For example, if the box's text is being rendered right-to-left, then the border-inline-start-color is applied to the right side of the border.

### Questions

1. Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?

I would section his blog into topics then color the individual sections and stylize the font in the sections.

2. What should you consider when choosing fonts for an HTML document?

Making sure the font is compatible with all browsers is a good start.

3. Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.

The foreground color is the text color and the backgriound color is the page color.

4. Describe two ways you could add spacing around the characters displayed in an h1 element.

Creating a new class in CSS and adding margins.

5. What do font-size, font-weight, and font-style do to HTML text elements?

Font-style is used to turn *italics* on or off. Font-weight shows how **bold** the text is. Font-size is how large the test is displayed

### Items I need to learn more about

- CSS Spacing
- Image files

### Resource links I Used

[Applying color to HTML elements using CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Colors/Applying_color)

[Images in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)

[Image file type and format guide](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types)

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
