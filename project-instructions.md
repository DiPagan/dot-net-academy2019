# Project instructions & requirements

### Scope
You have been given the task to create a new Vacation Rental platform for Northern Greece on the Web.
Owners of vacation homes and apartments can list their properties and the available dates for rental,
and vacationers can search the platform, find a desired place, and book it.  

Of course there are currently other competitors with similar web applications, but you will be building yours with the best technologies we learned during the lectures – with the stellar design and functionality that your application will offer, tourists desiring to spend their vacation in to Northern Greece will clearly choose yours!

The core of the application is the Search functionality, where tourists will look for the perfect rental to live their myth in Greece.  Vacation homes and other properties will be displayed in an attractive and simple-to-read way, luring the tourist to click “Book now”.


### Specifications
The following are the functional specifications of the project:

#### AUTHENTICATION
- Users need an account and cannot use the application if they are not authenticated
   - Unauthenticated users should only see information about what the site is all about, and the UI to Log In / Sign Up
- There are 2 types of users:
  - Owners
  - Renters (customers)
- Considerations
  - Can an Owner be a Renter of someone else’s property?
  - This is a community platform where users “do their job” without the need of central management – however, do we need to have an Administrator role to do “more mundane” jobs (e.g deactivate users, clean up old data)?

#### DATABASE DESIGN
- Vacation Properties should have at least the following characteristics:
  - Title (a short text to appear in search result and as the title in the property listing)
  - Description (a longer text, possibly in HTML format, to describe the property in more detail in the property listing)
  - Location (minimum requirement is a list of locations)
  - Maximum Occupancy (number of people that can stay)
  - Photo (1 main photo to be used as the profile picture of the property)
  - Owner (minimum requirement is just to display the name of the owner)
  - Price Per Night
- You should at least have one “detail” relationship for the Vacation Properties that depicts “Availability” for reservations
  - a list of date ranges that the property is available for rental (the owner might want to keep some days unavailable for maintenance or for his own usage)
- Reservations (Bookings) should have at least the following characteristics:  
  - Property
  - Renter (User)
  - Start Date
  - End Date
  - Number of Occupants
  - Date of Booking
  - Customer Comments
  - Price Per Night Charged
- *Bonus Points*
  - Other “detail” tables (such as a List of Amenities of the property)
  - Photo Gallery of the property
  - User Ratings of the property (submitted from the reservation form)
  - More complex pricing per night (based on number of occupants or dates belonging to different seasons)
  - More complex locations (either hierarchical e.g.  Halkidiki vs Halkidiki > Sarti, or storing coordinates to integrate with Maps)
  - Cancellation of Reservation (you will need to keep the “status” of the reservation – Active / Cancelled)

#### FUNCTIONALITY
- Sign Up / Log In Page
- Owners
  - View a list of «My Properties»
  - View the details of one Property
    - Ability to create a new property
    - Ability to edit the characteristics of a property
    - Ability to completely remove a property (if it has not been used in reservations) or make it “Inactive”/”Hidden” from the search functionality
  - View a list of «Reservations» for all the properties of the owner
- Renters
  - Search functionality / Search Results
  - View the details of one Property
    - Ability to make a reservation on available dates
  -	View a list of “My Reservations”  
- Considerations
 - What happens if there is a large number of properties?  Can the user get a list of all properties, or is there a “filter pane” to always reduce the amount of rows?
 - In the lists of reservations (for the owner and/or the renter) – does it make sense to always show all reservations, or only the ones in the future, making it one click further away to retrieve the past reservations?
- *Bonus Points*
 - Ability for a customer to cancel their reservation at any time
 - Ability for a customer to cancel their reservation based on a Cancellation policy that is submitted by the owner (e.g Cancel up to 1 / 7 / 30 days before)
 - Ability for an owner to deny a reservation  (you will need enhance the “status” of the reservation – Submitted / Approved / Rejected, and add any relevant fields – DenialDate, OwnerComments, etc)
 - Owner “Profile Page” where the renter can view a brief profile of the owner, a list of the properties, etc
 - Instead of a simple list (grid) of the reservations, show them in a calendar
 - Export reservations to a calendar (e.g Google Calendar)
 - Exchange messages (renter to owner and vice versa) before making a reservation and/or after making a reservation

#### DESIGN
- Modern web applications are Responsive – which means that all pages should look nice and be functional in most sizes / form factors
- Browser Compatibility – you can pick a “target browser”, but all pages should be functional for the top (“current”) browsers
- Look and Feel – your pages should be attractive!  Spend some time thinking about the layout, colors, etc
- Branding – pick a cool name and logo to better promote your site!
