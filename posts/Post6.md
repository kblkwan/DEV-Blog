---
title: A3 Reflection
date: 2026-06-13
author: Kieu-An Nguyen
summary: Strengths, limitations, and future improvements
tags:
  - Website Functionality
  - Evaluation of User Experience and Accessibility
  - Development Overview
---
‘After Dark’ is a community hub that helps users discover and connect with businesses, service providers, spaces, and opportunities available late at night. Instead of requiring people to fit their lives around restrictive operating hours, the platform supports greater flexibility and convenience by assisting users complete tasks and access services at times that better suit them. This project concept was inspired by my own experience of struggling to access services after work, and was designed to resonate with users who face similar limitations in their daily routines.

## Website Functionality
To reassess the original functional requirements, I compared the user flows defined during planning with the features the final prototype was realistically able to deliver. This helped clarify which requirements were realistic within the project scope, which features had to be simplified, and which functions would need further development before the platform could operate as intended.

The core features that are functional in the final prototype include:
- [ ] Create a new account
- [ ] Log in to access additional features
- [ ] Sign out of an account
- [ ] Create a post with a photo
- [ ] Create a request
- [ ] Search and filter content by posts, requests, and services
- [ ] Open a service listing and access its business profile page
- [ ] Send, receive, and reply to messages across different accounts
- [ ] Upload or change a profile picture
- [ ] View personal posts and requests on the profile page
- [ ] Interactive navbar and hamburger sidebar
- [ ] Explore nearby listings on an AI-generated map

#### Incomplete Features:
- Reviews are currently a placeholder, can’t be submitted and additional content does not load when you press ‘more reviews’
- Posts displayed on the business profiles are static images and do not redirect users to the relevant post page
- The settings page is a placeholder and does not currently include functional account controls

## Future Improvements

### Technical and Database Improvements
* [ ] Remove test data, duplicate records, and placeholder posts from the database
* [ ] Replace AI-generated placeholders with real user, business, and service data
* [ ] Ensure search results, profile photos, post counts, and request listings update dynamically

### User Experience Improvements
* [ ] Replace the AI-generated map with Google Maps
* [ ] Add map marker pop-ups so business details appear beside the map before users choose to open the full profile
* [ ] Replace the message recipient dropdown with a searchable user field and profile suggestions
* [ ] Improve responsiveness across mobile, tablet, and desktop screens
* [ ] Allow users to delete their own posts and requests
* [ ] Revise the design system to meet WCAG AA standards

### Future Feature Development
* [ ] Create business account features that allow service providers to customise their own profile pages
* [ ] Develop a business dashboard for managing customer requests, messages, and service listings
* [ ] Add basic social features such as liking, commenting, and sharing posts
* [ ] Add settings for text size, layout preferences, and accessibility controls

### Other
* [ ] Redesign the logo to better align with the After Dark brand identity


## Prototype Testing and Evaluation

### Pilot Test
A pilot test was conducted to validate the core functionality of the prototype, including website navigation, account access, content creation, and search. This helped verify whether the main user flows operated as intended and identify any immediate technical or usability issues. However, due to time constraints, broader user testing was not conducted, limiting the extent to which the overall user experience could be evaluated.

### Lighthouse Tests
I conducted Lighthouse tests across all pages to evaluate whether the website met basic accessibility standards. From these results, we identified two main accessibility issues in the design: insufficient colour contrast and hidden interactive elements that could not be properly detected by screen readers.

To address these issues, I would revisit the colour system using accessibility tools and design plugins to test contrast ratios across text, buttons, links, hover states, and background elements against WCAG AA standards. This is particularly important for a dark-themed interface, where secondary text and subtle UI states can easily become difficult to read if the visual style is prioritised over accessibility. I would also review the HTML structure, ARIA labels, and visibility settings of hidden or decorative elements so that screen readers can correctly identify meaningful content without being disrupted by interface elements that are not relevant to navigation or comprehension.

Additional usability issues were flagged on the Explore page, where several interactive map markers overlapped within the map interface. This reduced visual clarity and weakened the page’s usability, as users could not easily distinguish between nearby locations. The map was originally intended to use Google Maps as its source, but due to integration difficulties, an AI-generated map was used as a temporary substitute. In future iterations, Google Maps integration would allow markers to be clustered, filtered, zoomed, or expanded, helping users identify nearby services more efficiently while reducing visual clutter. I would also refine the page hierarchy so that location details, categories, and key actions are visually separated and easier to interpret.

### Chrome DevTools Network Load Test
Website load performance was evaluated using Chrome DevTools Network testing under consistent conditions, with the browser cache disabled and throttling applied across Slow 4G, Fast 4G, and No Throttling settings. While the application loaded efficiently without throttling, performance dropped significantly under constrained network conditions, particularly on the ‘Profile’ and ‘Search Results’ pages, which increased to 40.02 seconds and 1.5 minutes on Slow 4G. This suggests that the issue is not only caused by the testing environment, but also by how the website currently handles larger assets, user profile content, database-driven results, and image loading. As the platform scales, this may become a greater concern if more user-generated content, images, and search data are loaded at once. These findings align with image loading issues identified during development and indicate that future iterations should prioritise compression, lazy loading, asset optimisation, and more efficient data retrieval.

Add Image 



## AI-Assisted Website Development and Reflection

A key lesson from this project was that AI-assisted development still requires precise technical direction. While tools such as ChatGPT, Figma plugins, and Codex helped convert wireframes into a functioning prototype more efficiently, the process also exposed the limitations of relying on prompts without clearly defining system behaviour.

Add image

During development, I focused on building reusable components such as the navigation bar, page layouts, and repeated card structures. This helped maintain visual consistency across the site, but I did not clearly distinguish between static placeholders and content that should update dynamically from the database. As a result, some posts, requests, profile images, and numerical indicators were duplicated or remained disconnected from user-generated data. This weakened the credibility of the prototype because certain features appeared interactive but did not fully respond to user activity.

For future iterations, I would redefine the database structure, dynamic content rules, and placeholder logic before building new features. This process would include identifying which components should retrieve data from specific tables, which values should update through user interaction, and which elements are only temporary visual placeholders. I would also need to go back and clean up the database by removing duplicate records and outdated placeholder data so that new uploaded content does not get mixed in with the old. These changes would make After Dark feel more reliable, scalable, and closer to a real community platform.

## User Experience and Accessibility
Overall, the interface is mostly intuitive, particularly in areas that follow familiar web conventions. The login and create account pages are straightforward because they use recognisable form layouts, while the navbar, hamburger menu, and interactive buttons give users multiple ways to move between features. This makes the site easy to explore, even when users are not yet familiar with its structure.

However, the user experience is limited by the lack of rich data. While the prototype includes a functional database for users, posts, requests, services, and business information, it currently lacks the volume of organic content needed to demonstrate its full potential. Without enough user-generated data, the website functions more as a technical framework than a living community hub, limiting the depth of search results, recommendations, and interactions that would make the platform genuinely useful. As the database grows and more users upload content, the platform’s value would increase through stronger search results, more relevant interactions, and greater community activity. Responsiveness also remains a limitation, as several pages do not adapt well to smaller screens, which means the current version of ‘After Dark’ is only suitable for laptop and desktop use.

## Reflection
Upon reflection, some of the original development goals for After Dark were ambitious and could not be fully achieved within my current technical skill set and project timeframe. As a result, several intended features were represented through static images or AI-generated placeholder content, which communicated the intended functionality but did not provide the best user experience. In future projects, I would spend more time researching implementation strategies before development, particularly for complex features such as map integration, dynamic content, and data security systems. Working on this project taught me that a successful web application is not only defined by the number of features it includes, but by how reliably those features function, scale, and support real user needs.


## Appendix
<details>
  <summary>AI Acknowledgment</summary>
ChatGPT was used to help improve writing clarity, grammar, structure, and troubleshoot technical issues throughout my blog. All AI-generated content was reviewed and edited, and all design decisions and ideas are my original work.

This use of AI is acknowledged in accordance with the University of Sydney’s guidelines on generative AI in education (University of Sydney, 2024).
</details>
