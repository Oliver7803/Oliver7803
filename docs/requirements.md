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


| TODO: USE-CASE ID e.g. UC1, UC2, ... | TODO: USE-CASE NAME | 
| -------------------------------------- | ------------------- |
| **Description** | TODO: Goal to be achieved by use case and sources for requirement |
| **Actors** | TODO: List of actors involved in use case |
| **Assumptions** | TODO: Pre/post-conditions if any</td></tr>
| **Steps** | TODO: Interactions between actors and system necessary to achieve goal |
| **Variations** | TODO: OPTIONAL - Any variations in the steps of a use case |
| **Non-functional** | TODO: OPTIONAL - List of non-functional requirements that the use case must meet. |
| **Issues** | TODO: OPTIONAL - List of issues that remain to be resolved |


Use-Case diagram

[![Insert your Use-Case Diagram Here](images/use-case.png)](https://private-user-images.githubusercontent.com/344730781/684810338-5891d4f7-e090-49b2-944f-9209dd58fcc3.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3OTQ4Mjc5MDgsIm5iZiI6MTc5NDgyNzYwOCwicGF0aCI6Ii8zNDQ3MzA3ODEvNjg0ODEwMzM4LTU4OTFkNGY3LWUwOTAtNDliMi05NDRmLTkyMDlkZDU4ZmNjMy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYxMTE2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MTExNlQxMTEzMjhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1jYTYzOGM4MjIyZWNlYjg1MmVhOWQ5M2ZmOTIyNGFkMjg1MDA5MDJmMmNjMjRmZWY2OWMxZWZjNDdhNzMyMDQwJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.2JRgIFNZdXrQ3eJNiunsclufW8GMVtXVp1XvFaKCDFQ)<img width="1270" height="718" alt="image" src="https://github.com/user-attachments/assets/c4b2d387-a646-4a48-82aa-2559aba25420" />


## Software Requirements Specification
### Functional requirements
TODO: create a list of functional requirements. 
    e.g. "The system shall ..."
    Give each functional requirement a unique ID. e.g. FR1, FR2, ...
    Indicate which UC the requirement comes from.


### Non-Functional Requirements
TODO: Consider one or more [quality attributes](https://en.wikipedia.org/wiki/ISO/IEC_9126) to suggest a small number of non-functional requirements.
Give each non-functional requirement a unique ID. e.g. NFR1, NFR2, ...

Indicate which UC the requirement comes from.
