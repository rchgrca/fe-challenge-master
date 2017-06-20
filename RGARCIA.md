# Frontend Challenge

## Approach

* code for mobile first
* create element structure
* UX instincts are being considered:
  * use functional CSS approach (immutability, composability)
  * use multiple classnames in class attribute
  * increase speed of work with Basscss
  * clean, pleasant UI
    * gradient for visually pleasing effect, use BuildConnect "style guide"
    * sections:  
      * search
      * results
        * multiple listings: different style on hover
          * display single listing onclick
        * display "num listings" of "total listings" to increase user confidence
        * single listing display all data
        * single listing display laborTypes as links
          * onclick, display all listings with that laborType
      * laborTypes
        * hide laborTypes for all
          * frees up space on mobile
        * use checkboxes for multiple selections
    * interaction:
      * when typing in search box, delay sending request for 1 second, else no delay
      * use infinite scrolling
        * display 50 results
        * on scrollbar bottom, a request is send for the next 50 listings
