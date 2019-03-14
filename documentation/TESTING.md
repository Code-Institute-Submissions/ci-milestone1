# Testing

This document contains various tests, performed against the deployed Github Pages version of this project.

Additionally, throughout the development process I kept some rough notes on tests and issues done during the process. For sake of completion I have included these at the bottom of this document as Appendix A.

## Tests
### General Tests
##### Header/Footer Links
Go through all pages and test nav links and social media links in header and footer:  

- Index
- Discography
- Albums
	- The Monkees
	- More Monkees
	- Headquarters
	- PACJ
	- Birds, Bees, Monkees
	- Head
- Media
- Book us
- Thanks

##### Responsive Design
Go through all pages and check how they look at different screen widths:  

- [page list]
	- [width list (mobile, tablet, laptop (720p), desktop (1080p), large desktop (4k)]
- Index
	- Mobile (<768px)
		- 
	- Tablet (>768px)
		- 
	- Laptop (>992px)
		- 
	- Desktop[1080p] (>1200px)
		- 
	- Desktop[4K] (>2500px)
		- 
- Discography
	- Mobile (<768px)
		- 
	- Tablet (>768px)
		- 
	- Laptop (>992px)
		- 
	- Desktop[1080p] (>1200px)
		- 
	- Desktop[4K] (>2500px)
		- 
- Albums
	- NB: All use some layout
	- Mobile (<768px)
		- 
	- Tablet (>768px)
		- 
	- Laptop (>992px)
		- 
	- Desktop[1080p] (>1200px)
		- 
	- Desktop[4K] (>2500px)
		- 
- Media
	- Mobile (<768px)
		- 
	- Tablet (>768px)
		- 
	- Laptop (>992px)
		- 
	- Desktop[1080p] (>1200px)
		- 
	- Desktop[4K] (>2500px)
		- 
- Book us
	- Mobile (<768px)
		- 
	- Tablet (>768px)
		- 
	- Laptop (>992px)
		- 
	- Desktop[1080p] (>1200px)
		- 
	- Desktop[4K] (>2500px)
		- 
- Thanks
	- Mobile (<768px)
		- 
	- Tablet (>768px)
		- 
	- Laptop (>992px)
		- 
	- Desktop[1080p] (>1200px)
		- 
	- Desktop[4K] (>2500px)
		- 

##### UX
User stories, and how this project fulfils their needs:

1. As a fan/client, I want to visit an About Section, so I can learn about the band.
	1. Visit website, this takes them to the index page
	2. Band info and info about the band's members is on this page
2. As a fan/client, I want to visit a page of the band's music, so I can listen/watch previous performances.
	1. Go to "Discography" page
		- Info about the band's albums can be accessed through the individual album links
			- These album pages contain a track list
			- and sample song(s)[if applicable]
	2. Go to "Media" page
		- Watch videos in 'Video' section
		- Listen to sample songs in 'Audio' section
3. As a fan/client, I want to visit a page with photos of the band, so I can look at photos of the band/previous performances.
	1. Go to "Media" page
		- Photos of the band, etc. are located in the 'Images' section
4. As a client, I want to be able to contact the band, so I can discuss booking them.
	1. Go to "Book us" page
	2. Complete form
		- Fields suggest what to input
	3. Press submit
	4. Form is validated
		1. If validation fails: form gives reason and suggests corrections
		2. Else if validation passes: user is taken to a confirmation page

### Page Specific Tests
##### Index/About
N/A

##### Discography
Test album links link to correct page

##### Albums
Go through all pages, check audio player (if applicable) plays correct song.

- The Monkees
- More Monkees
- Headquarters
- PACJ
- Birds, Bees, Monkees
- Head

##### Media
1. Check video plays
2. Check audio players play
3. Check image thumbnails open correct image, this should be in a new tab

##### Contact
1. Check required fields give error if blank
	1. [req'ed field list]
2. Check data validation
	1. Phone should be numbers only
	2. Email should check input is valid email format
	3. Other fields are strings (do not need testing)
3. Valid form should successfully submit and give success message

##### Thanks
N/A



## Issues of Note

##### 4K requirement

1. Transform Scale
2. Zoom
3. Font size

##### Github Pages deployment

Root path



## Appendix A: Old Notes
- CSS
	- About Band (index)
	- Album info
		- ~~FAIL: CSS not loading~~
			- ~~Fix: Changed pathing on CSS links ~~
	- Booking
	- Discography
	- Media 
- Test header & footer links
	- Navs
		- About Band (index)
		- Album info
			- ~~FAIL: Links are pathing incorrectly~~
				- ~~Fix: Change HF links to path up one level~~
		- Booking
		- Discography
		- Media  
	- Social
		- About Band (index)
		- Album info
			- ~~FAIL: Links are relative and not working~~
				- ~~Fix: Change HF links to path up one level~~
		- Booking
		- Discography
		- Media 
- Page Content
	- About Band (index)
		- ~~FAIL: Right side images merged with text~~
			- ~~Fix: Pushed cols need other col Pulled~~
	- Album info
	- Booking
	- Discography
	- Media 
- Test responsive design
	- About Band (index)
		- ~~footer doesn't reach bottom of page at full width on 1080p~~
			- FIXED: created main-body-content class to apply min-height: calc(100vh - 225px)
	- Album info
		- ~~FAIL: Audio controls overlap tracklist on small screen widths~~
			- ~~FIX: Changed col-sm to col-md~~
	- Booking
	- Discography
		- ~~Would look better splitting into two columns at smaller screens~~
	- Media 
		- ~~Apply same responsive design improvements from discography~~
- Deployment to github pages
	- ~~GH-P's root directory doesn't include repo subdirectory, this breaks absolute links.~~
		- changed paths to relative links and used '../' to path up one level where needed
	- favicon not loading due wrong url on GHP
		- set favicon path in HEAD