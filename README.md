# Die Gefährten des Greifen e.V.
This is the code repository for the website of the association "Die Gefährten des Greifen e.V.". Below are technical information to help future members manage the website.
If you're looking for user-friendly documentation on how to update the content of the website, refer to https://die-greifen.github.io/die-greifen-webseite/

## Grav
The website is base on [Grav](https://getgrav.org/).
Grav has been choosen because it as "Flat-File" system : there are no software to install or databases to configure. Everything that the website needs is contained within this repository. This also makes it easy to move the website to a different host.
The actual documentation on how to manage the website is therefore the [Grav documentation](https://learn.getgrav.org/17). In this file are only a few informations to help members of the association to update the parts of the website that require code update because they can't be changed through the admin page. 

## This repository
This repository contains the website base : Grav, the theme ([Receptar](https://github.com/getgrav/grav-theme-receptar/tree/master)), and some of the content.
Although the repository contains the page's content, changes made to said content through the admin page are not automatically reflected in this repository. It is recommended to commit those changes regularly, as it provides a safe backup and a change history.

## Hosting
At the time of writing, the website is hosted on hosteurope.de on a WebHosting Medium.
If the website needs to be hosted somewhere else :
- Access the current server with FTP. The credentials are available through the hosteurope account. 
- Download the entire folder containing the website (probably /www/www.diegreifen.de/).
- Upload said folder to the new server

## Documentation
This README file contains the technical documentation. 
The "docs" folder contains the user documentation, accessible with GitHub Pages [here](https://die-greifen.github.io/die-greifen-webseite/)

## Updating content
Some parts of the website can't be changed with through admin page and require to update the files manually. Don't forget to commit the changes to this repository.

#### Social media links
Social media links are stored in user/config/site.yaml
See [here](https://github.com/getgrav/grav-skeleton-receptar-site/blob/develop/config/site.yaml) for an example with more websites

#### Page title
The title at the very top of the page is under user/themes/receptar/languages.yaml

#### About
The content of the "About" part of the menu is under user/pages/sidebar/about/widget.md