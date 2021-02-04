# User documentation
This page intends to help members of the association Die Gefährten des Greifen e.V. manage the content on their [website](www.diegreifen.de). 

## Login to the admin page
First, you need to login to the admin page. At the time of writing it is under http://diegreifen.de/preview/admin

A special user has been created for updating the content of the website. Ask other members of the association for the username and password. This user has limited rights on the admin page : it can only change the website's content. This way, in case of mistakes, you can only break the pages that you edited, the website in general will still work. If in doubt, ask first for an admin to make a backup of the website before editing.

Once logged-in, go to "Pages" on the left menu.

## Creating a new page 
You can create a new page with the "Add" button on the top right. 

Once you fill in the title, the folder name is automatically generated. Don't change it.

If you want the new page to be under another one, for example if you want a new square in the front page, choose the parent page by clicking on the "Parent page" field.

There is a long list of page templates, but only 3 are relevant : Blog, Default and Default alt.

## Page templates
There are 3 page templates (or layout). They can be choosen when creating a page or changed under the  "Advanced" tab when editing a page's content.
<dl>
	<dt>Blog</dt>
		<dd>This is a homepage-style layout. An optional full-width banner at the top and a grid of sub-pages.</dd>
	<dt>Default</dt>
		<dd>A content page with some text on the left side and a big image on the right side.</dd>
	<dt>Default alt</dt>
		<dd>The standard page without the big image on the left</dd>
</dl>
 
## Page content and formatting
Editing the pages content is done using "Markdown". You can check the full documentation [here](https://learn.getgrav.org/16/content/markdown), but it's a bit long. You may prefer checking the example page "Style Guide" under "Startseite", or just use the buttons at the top of the editing field.

You can preview the result without saving it by clicking the eye on the top-right of the editing field.

## Images
You can add images to the page. First, drag&drop the image in the "Page Media" field below the text editing field. Then add the image to the text like so :
```markdown
[ALT_TEXT](FILE_NAME)

```
Replace ALT_TEXT with the alternative text that is displayed in case the image fails to load. It is also used by accessibility software.
Replace FILE_NAME with the exact name of the file you placed in "Page Media".

You can include a small version of the image that can be clicked to a see the bigger version like this:
```markdown
[ALT_TEXT](FILE_NAME?lightbox=BIG_WIDTH,BIG_HEIGHT&resize=SMALL_WIDTH,SMALL_HEIGHT)
```
Replace BIG_WIDTH, BIG_HEIGHT, SMALL_WIDTH, SMALL_HEIGHT with the corresponding sizes in pixel.

## Pages with sub-pages
### Content
Pages with the "Blog" template, like the homepage or the Mitglieder page, don't have their own content. Instead they show a preview of their subpages.

The text preview is automatically taken from the text content of the subpage.

The image preview uses the first image available in the "Page Media" field of the subpage.
### Setting the banner image
By default, the "Blog" template includes a banner image. To set the image you want, first place it in the "Page Media" field. Then, switch to the "Expert" view with the button on the top-right. You then have a new field "Frontmatter" above the page's content field. Look for a line that looks like this, or add it if needed :
```yaml
banner: FILE_NAME
```
Replace FILE_NAME with the exact name of image you added just before.
### Removing the banner image
If you just want the list of sub-pages without the banner, go to the "Advanced" tab (in Normal view, not Expert), and in "Body Classes" add "hide-banner"
### Sorting the subpages
On the "Advanced" tab, on the right side, you can order the subpages.