# AEM GUI Project

 As this project was developed during my internship, the source code and application are considered confidential, and I cannot share the codebase or finished product. Instead, this documentation focuses on the project requirements, my responsibilities, the technologies I used, and the problem-solving process I followed

## Overview
During this project, I had the opportunity to dive into Adobe Experience Manager (AEM), a platform I was unfamiliar with before. The main goal was to improve a custom graphical user interface (GUI) designed to make it easier for developers to create content fragments in AEM. While the platform itself offers built-in tools for this, I found that the process can be cumbersome and confusing, especially for new users. The custom GUI we were working on aimed to streamline this workflow, making it faster and more intuitive, ultimately saving time and boosting productivity.  

My role primarily involved testing the application on AEM and using JavaScript and CSS to identify and fix bugs in the GUI. In addition to this, I proactively designed and implemented a new feature that allows users to quickly duplicate content fragments, further reducing repetitive manual work and enhancing usability. To make this happen, I had to carefully analyze current workflows, understand what users needed, and come up with a practical solution that would benefit the team in the long run.

## Notes
Although I received a debriefing on the project before starting, I wanted to fully understand its intent and the concepts involved. To achieve this, I began by researching AEM and content fragments, and I learned how to create them in AEM using the traditional method. This experience highlighted the importance of the GUI, as I saw firsthand how time-consuming the manual process can be. To reinforce my learning, I also took notes on the topics I explored. 
 
### What are Content Fragments? 
- Structured content without design or layout 
- Contain text, metadata, and structured fields 
- Structure determined by Content Frag Model which acts as a blueprint for type of content 
- Great for headless architectures:  frontend UI is separated from the back-end logic 

### Advantages 

**1. Channel-Agnostic Content Delivery**  
- Write content once (product description, FAQs) —>  use it everywhere (website, mobile app, etc.) 
- No copy/paste or rewriting content for different platforms 
- Easy to edit & stays in sync because all have same source 

**2. Consistency & Reuse**
- Update once —> updates everywhere 
- If content frag used in several places , and a change occurs, change will propagate to all places 
- Keeps branding and updates consistent 

**3. Structured Content Empowers Personalization**
- Organized content —> smarter, more personalized exp. 
- Store structured content makes it easier for systems to understand, filter and customize 
- Deliver content to different users automatically 

### Content Frags vs. Experience Frags 

Content frags are just structured data  
> Typically used for reusable data  

Experience frags are content + design/layout  
> Typically used for sections of pages 

## Helpful Documentation
- [AEM Documentation](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/getting-started)
- [Content Fragments](https://nam12.safelinks.protection.outlook.com/GetUrlReputation)
- [Content Frags. Basics & Demo](https://www.youtube.com/watch?v=bj7yragTtNI&t=62s)