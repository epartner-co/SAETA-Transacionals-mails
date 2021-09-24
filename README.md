# Transactional mails templates
_This is the template for change the transactional mails in all the stores (*Probably the Design department make some changes and it will be necessary to change the structure of these default files*)_

Follow the steps for edit the mails:

1. Clone or Fork the [templates mail repository](https://github.com/epartner-co/transactional-mails)
2. Add or edit the style using the guide bellow ⬇
3. Be carefully with the **Considerations**
4. The [cart abandoned template](https://gist.github.com/HajdukSanchez/2302bac37dec6f49b5e1c2343d20f5b3) use the same steps for edit, but the HTML structure is different

The templates mails are based on ```global.html```


## Structure
### HTML
The Structure of the HTML file is divided by comments and contains the next sections:
- Header
- Banner Top
- Text on the top
- Breadcrumb Images
- Order number information
- Description boxes (Address and Payment methods)
- Products details
- Payment values and information
- Button finish purchase
- Icons with information
- Footer

`Each one of these sections contains vital information of the mails.`

### CSS
The Structure of the CSS file is also divided by comments and contains the next sections:
- Variable colors and fonts
- Globals styles
- Specific Styles
- Header
- Main Banner
- Text top
- Breadcrumb images
- Order Number
- Boxes payment method and address shipping
- Product List Shipped
- Payment information values
- Button cart abandoned
- Icons container bottom
- Footer
- Socials Buttons

`Each one of the sections contains styles for specific components and blocks inside the HTML.`

## Guide for edit the templates
### Steps for edit the HTML 👷‍♂️
1. Add the new fonts using the ```<link>``` tag.
2. Inside the _'Style Sheet' Comment_ add the ```<style>``` tag and put the CSS inside them.
3. Go inside the _Header section_ and change the image tag source for the Company logo. ```<img src="{new-source}">```
4. Go inside the _Banner section_ and change the image tag source for the Top Banner. ```<img src="{new-source}">```
5. Go inside the _Top Text section_ and change only the text inside the tags but out of the {{}} keys.
6. Go inside the _Images Breadcrumb section_ and change the images tag source in each one of the images. Then it is important to add the Modifier Class ([BEM Methodology](http://getbem.com/)) inside the ```<div>``` tag and inside the ```<p>``` tag for change the text color and the line image color.
7. the Button finish purchase only appear in one of the templates, so if you are not creating the Cart abandoned template, fill free to delete it.
8. Go inside the _Icons data section_ and change each one of the icons and his informational text depends on the design.
9. The _Footer section_ always change depends on the design, so this block it is important to customize (don't forget to use [BEM](http://getbem.com/) for that) as we need in our design.

### Steps for edit the CSS 💅
1. On the ```:root``` rule, it is important to change the colors palette for each one of the developments (we use the SIKA color palette for this development) and also change the font family values.
2. Navigate between all the rules divided by comments and change the ```font-size``` declarations for those one in the design.
3. Fil free to change the rules declarations. (this one is an default and personalize standard).

### Edit the HTML mail in VTEX ✨
Google and other Mails providers block some styles of the tag Style, so once we have our style in each one of the templates, it is necessary to convert the style into inline html styles. Personally we use [mailchimp](https://templates.mailchimp.com/resources/inline-css/) for convert the HTML and CSS into inline html styles.

After you make this inline styles it is necessary to change the VAR styles values in your inline styles. It is necessary to put the colors and styles without using the VAR in each one of the inline styles.


## Considerations 🚧
* Don't delete the ```<table>``` tag childs as ```<td>``` or ```<tr>``` tags. Because probably you will be broke the VTEX default functionality.
* Don't delete the content inside the {{}} keys, but if you do, please be carefully and make exhausted tests.
* Use the [BEM Methodology](http://getbem.com/) if you want to make changes in your development, or if you are going to add and extra block.
* The entire development classes was created using [BEM Methodology](http://getbem.com/).
* This is the general template and contains all the elements presents on the transactional templates mails. You can copy and paste this code, and make some few changes for your development and for all the transactionals mails that we use.
* If you are going to change the colors, select all the css declarations that use this color and change the name of the color respectively, use the colors name for more legibility. Then change the color variable value.
* The *Style.css* file contains the backup styles that come by default.


_[The original templates](https://github.com/epartner-co/transactional-mails)_

_Code with ♥_
