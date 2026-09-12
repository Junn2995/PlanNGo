# Plan N Go by Workers and Musician
Team: Lim Zi Jun, Cheah Mun Xi, Lee Shu Wei, Wong Zhi Yun

Problem Statement: Travel Planner

[Video Presentation](https://youtu.be/GmQBcq0IxCU)

[Presentation Slides](https://canva.link/gg35gqv95leqt68)

## 1. Project Overview
### The Problem
Most of the travel planning requires users to book  flights, hotels, activities, and other travel services separately. This can make the planning process complicated and confusing, especially when users do not have a clear overview of their entire trip. Even with a well-planned itinerary, unexpected situations such as flight delays or weather changes can disrupt the whole plan and require users to reorganize their schedule.

Besides that, for group travel, the person responsible for making the bookings may also face significant financial pressure. They may need to pay the full amount upfront, while their friends may delay or fail to pay them back, causing financial loss and affecting their relationships. 

Group members may have different preferences, making it difficult to create an itinerary that satisfies everyone. Without a proper preference-matching system, the final plan may favor certain members while overlooking the interests of others.

Nowadays, many people have busy schedules, making it difficult to find a suitable time when everyone is available to meet and travel together. Existing travel planning applications often require users to select specific dates, which can make group trip planning more difficult when members have different schedules. As a result, finding a date that works for everyone can be time-consuming and challenging.

Furthermore, the visually impaired travellers may face difficulties when travelling alone, especially when navigating unfamiliar places safely. Although there are existing applications that provide assistance, such as short-distance navigation or video-call support, these services may not provide continuous, end-to-end assistance throughout the traveller’s journey.

### Our Solution
Our system simplifies the travel planning process by combining multiple travel features into one platform. Users can select the required features sequentially and make the payment through the system.

Besides that, to reduce the financial pressure on the person responsible for making the booking, we provide a separate payment system where each group member is required to pay their own share. Once all group members have completed their payments, the booking will be confirmed.

To accommodate the preferences of most group members, we provide a preference-matching system that analyzes each member's preferences and generates suitable recommendations. We also allow users to select their available and unavailable dates, making it easier for the group to find a suitable time to travel.

For visually impaired travellers, we provide an option to choose a verified volunteer to accompany them throughout their trip. This can reduce the anxiety and risk of getting lost when travelling in unfamiliar places.

## 2. Ideation & Process
### 2.1 Ideas We Considered
<table border="1">
  <tr>
    <th>Idea</th>
    <th>Why it was dropped / kept</th>
  </tr>
  <tr>
    <td><b>Combine All Features in a Plan (Chosen)</b></td>
    <td>Solved the problem of using multiple platforms for flight, hotel, activities and car rental. Users can plan and book the whole trip and make one combined payment.</td>
  </tr>
  <tr>
    <td><b>Group member date matching (Chosen)</b></td>
    <td>This function finds overlapping dates when all group members are available. Other platforms only allow choosing dates by one person, which makes it hard to coordinate schedules.</td>
  </tr>
  <tr>
    <td><b>Group preference matching by rating (Chosen)</b></td>
    <td>This system can identify activity categories that members like or dislike most. This helps AI use those preferences to generate the best-matched trip plan.</td>
  </tr>
  <tr>
    <td><b>Separate payment system (Chosen)</b></td>
    <td>The system can calculate each member's share. After all members' payments are completed, the booking will then be complete. This makes the cost transparent and avoids confusion about how much each person needs to pay.</td>
  </tr>
  <tr>
    <td><b>Volunteer Travel Companion (Chosen)</b></td>
    <td>Provides trained and company-certified travel companions for visually impaired solo travellers.</td>
  </tr>
  <tr>
    <td><b>Flight delay & Weather change notification + AI change plan (Chosen)</b></td>
    <td>The system notifies users when flight delays, cancellations, or significant weather changes may affect their trip. AI identifies which parts of the itinerary may be affected and suggest or generate an updated travel plan based on the changes. This helps users respond quickly to unexpected changes during their trip. </td>
  </tr>
  <tr>
    <td><b>Travel Diary (Chosen)</b></td>
    <td>Allows users to record their travel experiences, photos, notes and memories for both solo and group trips. For group trips, members can contribute to a shared diary. Users can look back at their memories and experiences even years after the trip.</td>
  </tr>
  <tr>
    <td><b>Chat Function (Dropped)</b></td>
    <td>Useful for communication, but users can use existing messaging apps to communicate. Also, it is not central to the travel-booking problem.</td>
  </tr>
  <tr>
    <td><b>Polling Function (Dropped)</b></td>
    <td>Could help groups vote on destinations or activities, but the group preference matching function already provides a more direct solution and is similar.</td>
  </tr>
</table>

### 2.2 Ideation Boards
We created a shared Google Docs where everyone could contribute and record their ideas. After gathering the ideas, we organized and discussed them to identify the most suitable ones for our project. We then created a flowchart using draw.io to visualize the overall process and ensure that all team members had a clear understanding of the proposed flow. Although the flowchart may differ slightly from our current ideas, it helped us identify areas that needed to be refined. We also discuss and refine our ideas through face-to-face discussions.
![Google Docs](/images/docs.png)

![Flow Chart](/images/flowchart.png)

### 2.3 Mentor Consultation
<table border="1" cellpadding="8" cellspacing="0">
  <tr>
    <th>Date</th>
    <th>Mentor</th>
    <th>Feedback Received</th>
    <th>What Was Changed</th>
  </tr>
  <tr>
    <td>08/09/2026<br>20:25 Slot</td>
    <td>Lim Zi Yang</td>
    <td>
      • The current features are too similar to existing applications such as Trip.com.<br><br>
      • Conduct more research to determine the direction we want to take.<br><br>
      • Focus more on the core features rather than UI/UX design.<br><br>
      • Use tools that can help us find inspiration.<br><br>
      • Explore more unique features to differentiate our application from existing applications.<br><br>
      • Create a workflow.
    </td>
    <td>
      • We spent more time conducting research to identify problems that most existing applications do not address.<br><br>
      • We optimized the ideas we had.<br><br>
      • We reorganized the overall flow of our idea to make it more realistic, smooth, and clear.
    </td>
  </tr>
</table>

## 3. Design & Prototype
[UI Prototype](https://www.figma.com/design/9BV0odo3YyZJ2xKZQtlXCO/Untitled?node-id=0-1&t=92VUABxRGtTvp1xN-1)

## 4. What Make It Different
### Real-Time Contingency & Dynamic Itinerary Adaptation
The Concept: Automated, real-time recalculation of itineraries based on external travel disruptions (flight delays or weather changes).

The Twist / Originality: Existing apps send static notifications when flights are delayed. Our system automatically rewrites the live schedule using a smart prioritization hierarchy: it automatically shifts or discards unbooked/ticketless activities first, preserving paid reservations wherever possible. Weather shifts trigger instant indoor/outdoor activity swaps to protect the user's travel time and budget.
### Inclusive "Sight-Guide" Companion System (OKU / Blind Accessibility)
The Concept: Integrated booking for verified, certificated volunteers to accompany visually impaired (OKU) solo travelers throughout their daily travel journey.

The Twist / Originality: Apps like Travel Hands (London) provide point-to-point micro-navigation (walking from station A to B), while Be My Eyes offers short virtual video assistance. Our platform integrates physical companion matching directly into full-day travel itineraries, keeping the blind traveler supported from morning departures until they return safely to their hotel.
### Post-Travel Automation: Turnkey Itinerary Templates & Memory Diaries
The Concept: Converting completed trips directly into shareable community templates and interactive photo/video diaries.

The Twist / Originality: It moves seamless trip generation beyond the planning phase. Rather than requiring users to manually author a guide, the system automatically sanitizes and publishes completed trips into re-usable, bookable templates for other users.


## 5. Technical Architecture & Feasibility
### Tech stack
- ### Frontend
Next.js (React) will be used for the frontend because it was recommended by our mentor and is suitable for building a modern web application. It allows us to create reusable components and handle different pages such as trip planning, group preferences, booking, payment and travel diary. 

Constraints: Our team has limited development time and experience with Next.js, so we will keep the implementation focused on the core features required for the prototype. 

- ### Backend
Next.js Server-side API / Route Handlers will be used as the backend layer of our application. It will handle requests between the frontend, Supabase database and external APIs, such as AI, flight and weather services. We chose this approach because it allows us to manage both the frontend and backend within the same Next.js project, reducing development complexity and the number of technologies our team needs to learn.

Constraint: Our team has limited experience with backend development and Next.js server-side features. Therefore, we will keep the backend focused on the core functions required for the prototype, such as retrieving and storing trip data, processing user preferences and connecting to external APIs.



- ### Database
We plan to use Supabase for storing user accounts, groups, trip information, preferences, bookings and payment status. Supabase is suitable for our project because it provides a database and authentication services with a free tier, which is useful for a student project. 

Constraints: The free tier has usage and storage limitations. We may also need to keep the amount of stored data and API requests within the available limits. 

- ### APIs
We will first use mock APIs to develop and test the application. Once the core functions are stable, we will replace the mock APIs with real APIs that are free and accessible. 

Constraint: Mock data will not represent real-time availability or prices. Therefore, the prototype cannot guarantee that the displayed bookings are actually available. 

- ### Services (Payment)
The payment system will be simulated for the prototype, it won’t connect directly to real banking services or Touch ’n Go accounts. Users can select a payment method and proceed through a simulated payment flow to demonstrate how the combined booking and group payment process would work.
For group trips, the system will calculate each member's payment share and display their individual amount.
Constraint: No real money will be transferred, and the prototype will not process actual bank or e-wallet transactions. A production version would require a proper payment gateway, security measures and merchant/payment-provider integration.

- ### Hosting
The web application will be hosted on Vercel, which is suitable for Next.js applications and provides a free tier for our prototype projects. It can allow us to deploy the application quickly and share a public URL with judges.
Constraint: The free hosting tier has limits on usage and server resources. These limits should be sufficient for our prototype but may not be suitable for a large number of real users.

### Overall Technology Approach
Our approach is to prioritize free and accessible technologies so that we can build and demonstrate the main concept within the project timeframe. Where real external services are not freely available, we will use mock APIs and simulated payment data rather than paying for commercial services. This allows us to focus on demonstrating the core features of our project.


### Build plan & scope
During the building phase, we will focus on developing the core travel planning flow for both solo and group travel. This includes manual trip planning and AI trip planning, where users can select flights, hotels, activities, and other travel options based on their preferences and budget.

For group travel, we will implement the group availability and preference-matching system, allowing members to submit their available dates, budgets, and preferences before generating a suitable itinerary. We will also demonstrate the separate payment system, where each group member pays their own share before the booking is confirmed.

In addition, we will demonstrate dynamic itinerary adjustment for unexpected situations such as flight delays and weather changes. The system will notify users and allow AI to rearrange or remove suitable activities before updating the itinerary.

For visual impaired travellers, we will demonstrate the volunteer selection flow using sample volunteers.

For functions that require APIs, we will try to use free APIs or sample data where possible instead of using paid services. For the payment system, we will only demonstrate the separate payment flow using simulated payments and will not process any real transactions.

## 6. Target Audience
### 1."Lazy Planners" & Efficiency Seekers
This segment consists of travelers who want to travel but hate spending hours researching routes, hotels, and tickets. To serve these users, the system leverages AI-generated instant trips, automatic budget optimization, and pre-built travel templates to make planning fast and effortless.

### 2.Group Travelers & Friends Splitting Expenses
This segment targets groups of friends, families, or colleagues planning joint trips together. The platform supports them by relying on automated expense splitting, transparent per-person budget tracking, and AI consensus matching to align preferences and avoid group conflict.

### 3.Visually Impaired (OKU) Travelers
This segment includes blind or visually impaired individuals seeking safe and independent travel options. The platform empowers these travelers by granting access to verified, certified volunteer "Sight-Guides" who provide full-day, door-to-door physical accompaniment throughout the trip to reduce anxiety and spatial navigation hazards in unfamiliar places.



