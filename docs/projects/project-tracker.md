# Project Tracker Overview

My first project at BCBS, challeneged me to work with several frameworks and technologies that I was unfamiliar with. I've laid out my approach to this assigment and what I learned from it. The project itself can be viewed on my [Github]().

## Setup
<!-- tabs:start -->
### **Node.js**
Check that you have node.js latest version installed:
  - Open command line prompt
  - Cd to folder where Node.js has been installed
  - Paste / type the following code:  
  ```code
  node -v  
  npm –v
  ```  
  If a version number does not show, follow the instructions [here](https://nodejs.org/en/download) to download Node.js.
### **Vue 3**
  Set up Vue Application
- Open Visual Studio Code  
- Run following code in terminal  
```code
npm create vue@latest
```
- Answer the following questions as indicated below:

```text
Name your project: Enter project name
Add TypeScript? Yes
Add Vue Router? Yes
Add Pinia for state management? Yes
```
All other questions are up to user discretion  
- cd to newly created project  
- Run the following commands:
```code
npm install
npm run dev
```
> For additional help with getting started visit [this website](https://vuejs.org/guide/quick-start.html)

### **Jest**
Install Jest for Vue 3 project
- Open Vue 3 project in VS Code
- Open new terminal
- Run the following command
```
npm install --save-dev jest
```
> For additional help with Jest, visit [this site](https://jestjs.io/docs/getting-started)
<!-- tabs:end -->

## Project Details
### Overview
Build a small web application called Team Project Tracker using the tools and frameworks our team uses for frontend development.
The project tracker should allow users to manage and view a list of team projects.

### Technology Requirements
You must use:

 - Vue 3
 - TypeScript
 - Pinia (state management)
 - PrimeVue (UI components)
 - npm
 - Git workflow
 - Jest (unit testing)  

### Application Features  

Your application must include the following:

<!-- tabs:start -->
### **Displays**
### List Projects
Display a list of projects where each one shows:
  - Name
  - Owner
  - Status
  - Due date  

### Summarize Projects
Display a summarized version of the projects, including: 
- Total projects
- Not Started count
- In Progress count
- Complete count

### **Data Manipulation**
### Search
- Add a search input
- Filter projects by name
- Search updates results as the user types  

### Filter
Add a dropdown to filter by the following status:
 - Not Started
 - In Progress
 - Complete  

### Add Project
Create a form to add a new project.  
Required fields:
- Name
- Owner
- Status
- Due date
- Description  

### Edit Project
- Allow editing an existing project
- Use the same form as "Add Project"


### Delete Project
- Allow users to delete a project
- Show a confirmation before deleting

### **View Details**
Clicking a project should open a dialog and display the following:
- Name
- Owner
- Status
- Due date
- Description

<!-- tabs:end -->

### Data Model
Use the following structure
```
export type ProjectStatus = 'Not Started' | 'In Progress' | ‘Complete’

export interface Project {
id: number
name: string
owner: string
status: ProjectStatus
dueDate: string
description: string
}
```

### State Management (Pinia)
Use Pinia to manage:
- project list
- search text
- selected status

Your store should:
- add projects
- update projects
- delete projects
- filter projects
- calculate summary values

### Unit Testing Requirements
You must include at least 4 Jest tests. With a stretch goal of 80% code coverage

Examples:
- filtering logic
- summary counts
- add/update/delete behavior
- form validation

### Deliverables
- Personal Git Repository
- Code walkthrough
- Demo of working application running locally
- Demo of Jest tests running successfully

### Stretch Goals (Optional)
If you finish early, you may add:

- localStorage persistence
- toast notifications
- sorting
- highlighting overdue projects
- improved UI styling

### Documentation
- Vue 3
  - [VueMastery](https://www.vuemastery.com/courses/intro-to-vue-3-comp-api/components-and-props-comp-api/)
  - [VueJS Docs](https://vuejs.org/guide/introduction.html)
- Pinia
  - [Pinia Docs](https://pinia.vuejs.org/introduction.html)
  - [Pinia Cheat Sheet](https://www.vuemastery.com/pinia/?coupon=PINIA-DOCS&via=eduardo#cheat-sheet)
- TypeScript
  - [TypeScript Docs](https://www.typescriptlang.org/docs/)
- Jest
  - [Getting Started](https://jestjs.io/docs/getting-started)
  - [Using Matchers](https://jestjs.io/docs/using-matchers)
  - [Globals](https://jestjs.io/docs/api#methods)
  - [Expect](https://jestjs.io/docs/expect#expectarrayofvalue)
- npm
  - [npm Docs](https://docs.npmjs.com/)
