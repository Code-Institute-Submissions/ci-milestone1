# Milestone 1 Project: Band Website

The client, a 60s rock band, has requested a website creating to promote their band. 

The primary purpose of this is for their fans, past and future, to view media (photos, audio, and videos) of the band's past and future works, and information about the band (including links to social media).

The secondary purpose of this website will be to use it to promote the band to potential clients to hire them for events and gigs, by providing demonstrations of the band's capabilities and allowing a facility for the potential clients to contact the band in order to hire them.
 
## UX
 
### User stories
There are two main user types: fans and clients.

- Fans will want to visit the site for information on the band, view photos, listen to music clips, and watch videos.
- Clients will want all of the above, plus the ability to contact the band to enquire about booking them for events.

The site will be planned around the following scenarios:

1. As a fan/client, I want to visit an About Section, so I can learn about the band.
2. As a fan/client, I want to visit a page of the band's music, so I can listen/watch previous performances.
3. As a fan/client, I want to visit a page with photos of the band, so I can look at photos of the band/previous performances.
4. As a client, I want to be able to contact the band, so I can discuss booking them.

### Pages
The site will consist of the following pages:

- About - information about the band and band members.
- Discography - info of the band's albums.
    - ? Thumbnails of album cover art which link to individual pages for each album ?
        - ? Each album page has info (song list, release date) and a sample song(s) ?
- Media - videos, sample songs, and photos of the band.
- Booking - contact page advertising what sort of venues and gigs the band plays at and contact link/form for clients to book them.

The initial Wireframe mockups of the pages [can be found here](documentation/wireframes/wireframes.xlsx).  
After I became more adept with Bootstrap's grid system, I updated the wireframes to include plans for sub-grids. [Version 2 of Wireframes](documentation/wireframes/wireframesV2.xlsx).



## Features

### Existing Features

- Overall: 
	- Responsive design - by using Bootstrap I have been able to produce a website that fits comfortably on screens of all sizes. The pages dynamically adjust to fit: mobiles, tablets, laptops, and desktops.
	- Header & Footer navs bars - provides an easy way for the user to navigate between the main areas of the site, and also provides links to the various social media pages.
- Index.html - This is the 'About' page. Provides the user in User Story 1 information about the band and its members.
- Discography.html - This page contains a tiled list of the album's released by the band. Each tile is a link to a specific album's page.
- Album-*.html - This is a set of pages that hold information of a specific album. Here the user can look at the album's art, read the track list, or listen to a sample song (if available).
	- There is an 'album-boilerplate.html' file which acts as a template to produce additional album pages as needed in the future.
- Media.html - This page provides several subsections for the band's media, which the user in User Stories 2 & 3 are interested in. These are:
	- Videos - currently just one example video
	- Audio - tiles containing audio players to play sample songs. Each tile has the song name and the album it is from, the album name links to the album's discography page.
	- Images - tiles of thumbnail images. Clicking on a tile opens the full sized image in a new tab.
- Booking.html - This page consists of a contact form for potential clients (as in User Story 4) to contact the band to book them for an event.
	- Basic validation is applied to the form fields via HTML5's 'type' attribute.
	- Fields which are required are required through HTML5's 'required' attribute.
	- Placeholder text is used to instruct the user on what to enter into each field.
	- Upon submission the form redirects to a 'thanks' page to confirm the submission.


### Features Left to Implement

###### Short term: 

- Contact form is currently a dummy (not linked to a backend).
- The 'Thanks' page has a lot of white space, echoing the contents of the submitted form could be something good to take up that space.
- Social media pages all link to dummy pages instead of an actual page on the relevant social media platform.

###### Long term: 

- A merchandising page. Most bands have some form of online shop to sell albums and band merch. 
- A page with a calender that lists the band's gigs would be a good future feature. 
- Bootstrap 4 migration - when development on the project began, bootstrap 3.3.7 was the released version, and was the version covered by the course material, and so this was the version of Bootstrap used. During development of the project Bootstrap 4 was released.
	- The main advantage of Bootstrap 4 in regards to this project, is that Bootstrap 4 is designed better to support very large display widths (QHD and UHD).

## Technologies Used

###### Languages

- [HTML5](https://www.w3.org/standards/webdesign/htmlcss)
	- Latest version of the Hyper Text Markup Language, used to write the markup language the browser interprets to display the webpage elements 
- [CSS 4](https://www.w3.org/standards/webdesign/htmlcss)
	- Used to create style sheets to adjust the styles of HTML elements

###### Frameworks & Libraries

- [Bootstrap 3.3.7](https://getbootstrap.com/docs/3.3/)
	- CSS framework that provides a collection of prebuilt styles. The main use of this framework is the grid system it provides, as this allowed me to quickly develop the structure of the project's pages
- [FontAwesome](https://fontawesome.com/)
	- A large library of various icons, this was used to provide the social media link icons
- [Google Fonts](https://fonts.google.com/)
	- A large repository of free fonts. A nice feature of this site is that it recommends fonts that complement each other. This projects uses its two fonts from here (Happy Monkey and Raleway)

###### Tools

- [MarkdownPad 2](http://markdownpad.com/)
	- A text editor specifically designed for editing Markdown documents, provides a preview pane and syntax highlighting to make writing .md files easier. Used to produce this README.md
- [Cloud9](https://c9.io/)
	- Provides Linux workspaces which include an IDE for developing web based software, file hosting, git SVN, and basic web server services
- [MS Excel](https://products.office.com/en-gb/excel)
	- Spreadsheet software, used to create wireframes
- [Google Chrome](https://www.google.com/chrome/)
	- Web browser. Includes Dev Tools which provide information on how the elements are rendered, what style rules are applied, and allows editing of the HTML and CSS to see their effects live in the view pane. 
- [Irfan View](https://www.irfanview.com/)
	- Image Viewer. Provides tools for basic editing. Used to bulk resize project images.
- [Github](https://github.com/)
	- Hosting service for Git Software Version Controlled repositories. Also has a service called Github Pages, which provides web hosting to the repos. 
- [W3C Validator](https://validator.w3.org/)
	- Validates HTML markup files. Checks for errors in syntax such as unclosed tags or unneeded close tags.
- [W3C Jigsaw](https://jigsaw.w3.org/css-validator/)
	- Validates CSS files for syntax errors.

## Testing

Testing documentation is located in a [separate TESTING.md document](documentation/TESTING.md) located in the docs folder.

## Deployment

###### Run Local

Download & unzip or Git Clone to a directory of your choice.  
Open index.html in a browser of your choice.

###### Git Hub Pages

To deploy the website to github pages I did the following:

- Created a new gibhub repo
- Pushed to the github repo from my c9 workspace's local git repo
- On github, created a new branch called 'gh-pages'
	- At certain points in the dev process, pulled main branch to the gh-pages branch, this was to keep the Deployment Version stable, from the Development version which would likely contain WIP content
- In the github repo settings, went to the GitHub Pages section and set the source branch to the 'gh-pages' branch
	- This gives a hyperlink to the hosted version of the project

There are no differences between the development version (aside from the deployed version running from a separate git directory, which was largely for house keeping and not necessary to run the site), although several changes were made in the development process to make the site compatible with github pages.  
This was largely due to GHP's root directory being 'username.github.io/' instead of 'username.github.io/branchname/', so any absolute links would path incorrectly. 



## Credits

### Content
###### index.html
- id=band-info: text was copied from the [Wikipedia article The Monkees](https://en.wikipedia.org/wiki/The_Monkees)
- id=dj: text was copied from the [Wikipedia article Davy Jones](https://en.wikipedia.org/wiki/Davy_Jones_(musician))
- id=mn: text was copied from the [Wikipedia article The Monkees](https://en.wikipedia.org/wiki/Michael_Nesmith)
- id=pt: text was copied from the [Wikipedia article The Monkees](https://en.wikipedia.org/wiki/Peter_Tork)
- id=md: text was copied from the [Wikipedia article The Monkees](https://en.wikipedia.org/wiki/Micky_Dolenz)
 
###### /albums/album-*.html
- /albums/covers - track lists taken from wikipedia's respective page for each album, as linked on [Wikipedia's 'The Monkees Discography'](https://en.wikipedia.org/wiki/The_Monkees_discography#Studio_albums)


### Media
- Majority of photos used in this site were obtained from [Code Institute's project assets repo](https://github.com/Code-Institute-Org/project-assets)
- /albums/covers - album art taken from wikipedia's respective page for each album, as linked on [Wikipedia's 'The Monkees Discography'](https://en.wikipedia.org/wiki/The_Monkees_discography#Studio_albums)

### Acknowledgements

- I received inspiration for this project from [the offical Monkees website](https://www.monkees.com/)
- I received advice from my mentor, Chris Zielinski. 
