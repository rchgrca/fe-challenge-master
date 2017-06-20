# Frontend Challenge

## Approach

* code for mobile first
* create element structure
* UX instincts are being considered:
  * use functional CSS approach (immutability, composability)
  * use multiple classnames in class attribute
  * increase speed of work with Basscss
  * clean, pleasant UI
    * gradient for visually pleasing effect, use BuildingConnected "style guide" (http://buildingconnected.com)
    * sections:  
      * search
        * use orange call to action icon
      * results
        * multiple listings: different style on hover
          * display single listing onclick
        * display "numListings" of "totalListings" to increase user confidence
        * single listing, display all data details
        * single listing, display laborTypes as links for convenient filtering
          * onclick, display all listings with that laborType
      * laborTypes
        * hide laborTypes for all
          * frees up space on mobile
        * use checkboxes for multiple selections
    * interaction:
      * when typing in search box, delay sending request for 1 second, else no delay
      * use infinite scrolling
        * display 50 results
        * on scrollbar bottom, a request is sent for the next 50 listings
        * append new listings to current listings

## Accomplished

* While the user is typing in their search string don't actually send the query to the API until it's been 1 second since their last keystroke, so as to avoid sending a bajillion requests. (DONE)
* Don't use any basic utility libraries (e.g. jQuery, Lodash, Underscore, Ramda). (DONE)
* Don't use any front-end frameworks (e.g. React, Angular, Ember). (DONE)
* Search results should be pageable (or infinite scroll-able) (DONE)

If you have some spare time at the end here are a few stretch goals:

* Make your design responsive, so it works well across various device sizes (DONE)
* Focus on polishing the UI to look slick (DONE)
* Allow filtering results by labor type (DONE)

## Features

* Filter laborType by link found in single listing detail (eg: type 'Trane', click 'None', all listings with 'None' labortype are displayed)
* Click on LaborTypes header.  This would take up too much space for mobile so it's not displayed unless toggled
* The onkeyup event is used instead onchange for search input because it's a better user experience
* Added display of "numListings" of "totalListings" to enhance user experience

## Bugs

* You can continue to scroll past the limit (user sees "There are no results")
* You can filter on laborTypes of the entire data set only.  Filtering on a string first, then laborType is not possible
* There are a few tiny UI bugs (eg: items off by 1px)
* You can enter data beyond the search icon
