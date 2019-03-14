# Testing

This document contains various tests, performed against the deployed Github Pages version of this project.

Additionally, throughout the development process I kept some rough notes on tests and issues done during the process. For sake of completion I have included these at the bottom of this document as Appendix A.

## Tests
### General Tests
##### Header/Footer Links
Go through all pages and test nav links and social media links in header and footer:  

- Index
	- PASS
- Discography
	- PASS
- Albums
	- The Monkees
		- PASS
	- More Monkees
		- PASS
	- Headquarters
		- PASS
	- PACJ
		- PASS
	- Birds, Bees, Monkees
		- PASS
	- Head
		- PASS
- Media
	- PASS
- Book us
	- PASS
- Thanks
	- PASS

### Page Specific Tests
##### Index/About
N/A

##### Discography


- Test album links link to correct page
	- PASS

##### Albums
Go through all pages, check audio player (if applicable) plays correct song.

- The Monkees
	- PASS
- More Monkees
	- PASS
- Headquarters
	- N/A
- PACJ
	- N/A
- Birds, Bees, Monkees
	- PASS
- Head
	- N/A

##### Media
1. Check video plays
	- PASS
2. Check audio players play
	- PASS
3. Check image thumbnails open correct image, this should be in a new tab
	- PASS

##### Contact
1. Check required fields give error if blank
	1. Name
		- PASS
	2. Phone
		- PASS
	3. Email
		- PASS
	4. Message
		- PASS
2. Check data validation
	1. Phone should be numbers only
		- PASS
	2. Email should check input is valid email format
		- PASS
	3. Other fields are strings (do not need testing)
		- N/A
3. Valid form should successfully submit and give success message
	- PASS

##### Thanks
N/A



## Responsive Design
Go through all pages and check how they look at different screen widths:  

- Header
	- Mobile (<768px)
		- Logo at top, nav elements are 2x2, social elements are centred in row below nav elements
	- Tablet (>768px)
		- As above but: nav is 4x1, social row pulled to right
	- Laptop (>992px)
		- As above
	- Desktop[720p/1080p] (>1200px)
		- Logo on left, nav to right in 4x1, social below nav - pulled to right
	- Desktop[4K] (>2500px)
		- As above but: font and logo size doubled
- Footer
	- Mobile (<768px)
		- Nav links in 2x2 arrangement, social elements below nav and centred
	- Tablet (>768px)
		- Nav is on left, in vertical 1x4 arrangement
		- Social is on right, in vertical 1x3. Labels for the social media icons are revealed
	- Laptop (>992px)
		- As above
	- Desktop[720p/1080p] (>1200px)
		- As above
	- Desktop[4K] (>2500px)
		- As above but doubled in size
- Index
	- Mobile (<768px)
		- Infomation blocks are all full width under each other, band member photos are all on the left
	- Tablet (>768px)
		- About band block is full width with extra margins
		- Right side band member blocks: photo pushed to right, text pulled left
	- Laptop (>992px)
		- More l/r margins on About Band
	- Desktop[720p/1080p] (>1200px)
		- As above
	- Desktop[4K] (>2500px)
		- As above but doubled in size
- Discography
	- Mobile (<768px)
		- Ablum tiles are one under another
	- Tablet (>768px)
		- Album tiles go two per row
	- Laptop (>992px)
		- Album tiles go three per row
	- Desktop[720p/1080p] (>1200px)
		- As above
	- Desktop[4K] (>2500px)
		- As above but doubled in size
- Albums
	- ***NB: All use some layout***
	- Mobile (<768px)
		- Two full width blocks, vertical alignment
			- First has Cover art, audio player (if applicable) with track name under
			- Second has Track List
	- Tablet (>768px)
		- As above, but first block gets extra l/r margins
	- Laptop (>992px)
		- Two blocks go side by side
	- Desktop[720p/1080p] (>1200px)
		- As above
	- Desktop[4K] (>2500px)
		- As above but doubled in size
		- Issue: Images not retaining aspect ratio
			- Fix: Used CSS to set image height and max-height
- Media
	- Mobile (<768px)
		- Page has three sections
			- Video player is full width
			- Audio players are stacked, full width
			- Images - Thumbnails are stacked two per row
	- Tablet (>768px)
		- Video has l/r margins, centred in viewport
		- Audio changes to two per row
			- Issue: Two much horizontal white space, making boxes squashed
				- Fix: Changed col widths
		- Images: same as above
	- Laptop (>992px)
		- Video: Same as above
		- Audio: One row of three, used offsets to centre remaining audio block on second row
		- Images: Three per row, used offsets to centre remaining thumbnail on last row
	- Desktop[720p/1080p] (>1200px)
		- As above
	- Desktop[4K] (>2500px)
		- As above but doubled in size
- Book us
	- Mobile (<768px)
		- Has a paragraph about what the band does, full width
		- Form is full width
	- Tablet (>768px)
		- As above but with side margins
	- Laptop (>992px)
		- As above with bigger side margins
	- Desktop[720p/1080p] (>1200px)
		- As above with even bigger side margins
	- Desktop[4K] (>2500px)
		- As above but doubled in size
- Thanks
	- Mobile (<768px)
		- Page has a simple confirmation message, full width
			- There's a lot of white space under this message, it would be good to echo the contents of the submitted form here.
	- Tablet (>768px)
		- Adds side margins
	- Laptop (>992px)
		- Bigger margins
	- Desktop[720p/1080p] (>1200px)
		- As above
	- Desktop[4K] (>2500px)
		- As above but doubled in size

## UX
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



## Issues of Note

##### 4K requirement

During the submission checklist I became aware of the requirement to support very large screens (QHD and 4k), which Bootstrap 3 lacks proper support (as it uses PXes instead of EMs and other scalable functions)

I attempted to fix this by:

1. Using transform:scale(1.5) on the body tag to increase the size of all elements
	- This didn't work because elements were clipping outside of the viewport
2. Using Zoom on the body tag to increase size of all elements
	- This worked great on Chrome and Edge, but unfortunately is not supported by Firefox so I had to scrap this idea.
3. Font sizes
	- Eventually I gave up on being intelligently lazy and went for the simple approach of increasing the font sizes and image sizes by using a media query.
	- This fix is quite coarse as due to time constraints I have only done the main elements, I haven't done any fine adjustments such as margins and paddings

What I've learnt from this is to make use of EMs and Bootstrap 4 in the future, and that sometimes the simplest option is the best option.

##### Github Pages deployment

One issue I ran into when deploying onto Github Pages is that the root path for the site is [username].github.io instead of [username].github.io/[reponame].

This caused issues as I'd used /absolute paths in hrefs in the site, which the browser would translate into a path missing the repo name.

This was fixed by converting the paths to relative paths and using the '../' symbol to navigate the file structure where needed. 

---

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