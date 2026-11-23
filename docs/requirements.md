# Requirements

## User Needs

### User stories

- As a **Home owner**, I want to search planning applications by using my post-code or using my address so I can see what the progress of my own application is.
- As a **Member of the public**, I want to see a list of planning applications so I know which ones are the most likely to be approved and how often they are and if any are being refused.
- As a **Neighbour**, I want to search planning applications on a map to see what is being approved near me so that I can see planning in the area without knowing exact post codes or address and its easy to view.
- As a **Developer**, I want to search on a map planning applications to see what areas of Bristol have the most planning applications being approved so I know where the most construction is happening.
- As an **Analyst** I want to use the website to view data and analysis trends to write a report.
- As a **Council officer**, I want to make sure that the data is updated automatically so that people always have up to date automatic information.
  
### Actors

- **Home owner** - They search the site to check the status of their own planning application's.
- **Member of the public** - See planning applications in a list to know which are most likely to be approved.
- **Neighbour** – Can look up planning applications near there home to see what is being built near by.
- **Developer** – Use the site to see what planning applications are being approved and where.
- **Analyst** - views the statistics and other data to analyze trends in Bristol planning applications.
- **Council officer** - They don't use the website directly but they are responsible for managing the planning data and publishing it to Bristol Open Data which we then use on our website.
- **Bristol Open Data (external website)** – This is where we pull our data from for use on our website it is updated regularly and keeps all of our data up to date.
### Use Cases
TODO: Describe each use case (at least one per team member).
    Give each use case a unique ID, e.g. UC1, UC2, ...
    Summarise these using the use-case template below.

| UC1 | Search planning applications by postcode or address |
| --- | --- |
| **Description** | The user searches the website by postcode or address to check its progress  |
| **Actors** | Home owner, Bristol Open Data |
| **Assumptions** | Pre: the planning data has been loaded from Bristol Open Data ready to be accessed. Post: the user can see matching applications and their current status. |
| **Steps** | 1. User opens the search page. <br> 2. User enters a postcode or address. <br> 3. website checks the input is valid. <br> 4. website displays matching applications. <br> 5. website selects an application. <br> 6. website shows its details and current status. |
| **Variations** | 3a. Invalid postcode: website shows an error message as address is not valid. <br> 4a. No matches: system shows "No applications found" because there is no relevant applications. |
| **Non-functional** | Results should load within 2 seconds. Page should work on mobile. |
| **Issues** | Decide whether partial postcodes (e.g. "BS1") are allowed. |



| UC2 | See planning applications in a list |
| --- | --- |
| **Description** | The user looks at a large list of planning applications to see the frequency they are approved or refused. Source: Member of the public user story. |
| **Actors** | Member of the public, Bristol Open Data |
| **Assumptions** | Pre: the planning data has been loaded from Bristol Open Data. Post: the user can see a full list of applications and their status. |
| **Steps** | 1. User opens the list page. <br> 2. Website displays all applications. <br> 3. User selects an application. <br> 4. Website shows its details and current status. |
| **Variations** | 2a. User filters the list by status: Website shows only matching applications <br> 2b. User sorts the list by different option (size, newest first). Website reorders the list. <br> 2c. The list is too long for just 1 page: Website splits the list into multiple pages  |
| **Non-functional** | Results should load within 4 seconds. <br> Page should work on mobile. <br> Make it easy to read long list using colour coding green for approved red for refused.  |
| **Issues** | Decide how many applications are visible on each page. <br> Decide whether to show a count of each number of refused or approved applications. |



| UC3 | See planning applications on a map |
| --- | --- |
| **Description** | The user looks at a map of Bristol to see where planning applications are being approved and where the most applications are. Source: Developer, Neighbour user stories. |
| **Actors** | Developer, Neighbour, Bristol Open Data |
| **Assumptions** | Pre: the planning data has been loaded from Bristol Open Data. Post: the user can see a limited number of applications depending on where they look on the map. |
| **Steps** | 1. User opens the map page. <br> 2. Website asks the user to zoom in to see data. <br> 3. User zooms in to see data in the area of their choosing. <br> 4. Website shows data when they zoom in enough to see all of the pins easily. <br> 5. User clicks on a pin to see more details. <br> 6. Website displays details of planning application dependent on which pin they click. |
| **Variations** | 2a. Map data fails to load from Bristol Open Data: Website displays an error message. <br> 3a. User searches by postcode or area using search bar: Website displays pins in that area to see pins quickly without scrolling. <br> 3b. User uses a filter: Website displays data dependent on what filter used (Approved, refused, pending). <br> 4a. The user zooms into an area with no applications: Website displays a message no application data available. <br> 5a. User clicks a stack of pins: Website displays all details in a list. |
| **Non-functional** | Results should load within 4 seconds. <br> Page should work on mobile e.g. pinch to zoom. <br> Make it easier to see areas with the most data using colours such as red, orange and green depending on number of applications in one area.  |
| **Issues** | Decide how many pins are visible and when depending on zoom level. <br> Decide whether to stack pins displaying a number to see stacked planning applications easily and separate pins as the user zooms in closer. |

Use-Case diagram
<img width="1414" height="840" alt="image" src="https://github.com/user-attachments/assets/a8e0b77f-d301-4cd1-b099-3d7192dd6e5b" />



## Software Requirements Specification
### Functional requirements
- FR1: The system shall allow the user to search for planning applications using postcodes. (UC1)
- FR2: The system shall allow the user to search for planning applications using address. (UC1)
- FR3: The system shall display an error message for invalid postcode or address. (UC1)
- FR4: The system shall display a message when no relevant data is found. (UC1, UC3)
- FR5: The system shall display a list when a user clicks on the list page. (UC2)
- FR6: The system shall allow the user to filter the list by status of the application (approved, pending, refused). (UC2)
- FR7: The system shall allow the user to sort the list into different orders (newest, oldest). (UC2)
- FR8: The system shall split the list into multiple pages if the list is too long. (UC2)
- FR9: The system shall display a map when the map button is pressed. (UC3)
- FR10: The system shall show details on application when a pin is clicked. (UC3)
- FR11: The system shall show a list of application details when a stack of pins is clicked. (UC3)
- FR12: The system shall allow the user to search the map with postcode to move to areas of the map faster. (UC3)
- FR13: The system shall allow the user to filter the map pins via status. (UC3)
- FR14: The system shall allow the user to view the details on an application when clicked in a list. (UC2)
- FR15: The system shall load its data from Bristol Open Data and will display an error message for the website if it fails. (UC2, UC3)


### Non-Functional Requirements
- NFR1:



TODO: Consider one or more [quality attributes](https://en.wikipedia.org/wiki/ISO/IEC_9126) to suggest a small number of non-functional requirements.
Give each non-functional requirement a unique ID. e.g. NFR1, NFR2, ...

Indicate which UC the requirement comes from.
