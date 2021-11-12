# Purpose

Every engineering team is responsible for defining and clarifying their purpose. A purpose for every team is the compass that guides the team and ensures they stay on track.
Engineering teams should not identify their purposes as means. For instance, making profits is not a purpose in and of itself. But rather means to achieve higher aspects and bigger goals.
The ultimate purpose for every engineering team is to contribute to the survival of the humankind, it’s evolution and fulfillment. A team of engineers that keeps this purpose as their north start is destined to create the highest impact in their lifetimes and after.
But the purposing process requires intentional, systematic and deliberate efforts to define the material purpose. For instance, a team of engineers working on a restaurant software have to incorporate the fact that building efficient software falls directly into wading out someone’s hunger. The human impact is what connects us at the end of the day.
Purposing requires chasing the human impact regardless of whether it’s direct or indirect. For instance, building software for the turbo-machinery industry requires thinking about the people the software impacts. Building a simple human-machine-interface (HMI) will result in saving the workers who are going to be using the software’s time. Making their work environment safer. Expediting the production process therefore these workers become more productive.
Any software out there built to cause humans harm in terms of destruction, spreading misinformation, scamming people or replacing their daily jobs with automated processes without offering an alternative is a software that aims to the destruction of the humankind, it’s devolution and depression.
As software engineers we must always consider the human aspect of what we build. How does it largely impact beyond our immediate family but looking beyond that horizon and ensuring we are building healthy, productive software.

The purposing process requires these main aspects to be considered.
1.	Overall Purpose
2.	Scenarios
3.	Features
4.	User Stories
5.	Tasks
6.	Defects

The Standard Team is to clearly understand and define each and every aspect of the aforementioned points. 

## 1.0 Overall Purpose
The overall purpose of every project is what defines the boundaries of the project. For instance, if we are building a Bakery system, we need to define the following aspects:
-	Nature of the business
-	Goals of the business
-	Future considerations

### 1.0.0 Business Nature
The nature of the business is what defines what the business is. Our Bakery system would define it’s nature as follows:
A bakery is an establishment that produces and sells flour-based food baked in an oven such as bread, cookies, cakes, pastries, and pies.

### 1.0.1 Business Goals
Deliver the highest quality of bakeries to as many customers as possible.

### 1.0.2 Future Considerations
Expanding to become a nation-wide bakery business selling across the country.

These above three aspects should help the engineering team understand the nature, goals and potential growth of the business to ensure they build software that can support that expansion.
For instance, knowing that one of the goals of the business is that it will be nation-wide will help engineers determine whether to build a simple POS system running as a desktop application or a web application with mobile app capability to help customers order on-the-go as fast and as simple as possible.

## 1.1 Scenarios
Now that we have clarified the overall purpose of the business, we start going into scenarios where we talk about higher-level goals of achieving these purposes. Let’s talk about that.

Scenarios of any business are not meant to be technical. But they can dive into that level if needed. You shouldn’t expect any technical language in any given scenario unless the business itself is technical. Every scenario needs to fulfil the following aspects:
-	Actors (Given)
-	Interactions (When)
-	Outcomes (Then)

Here’s an example for a scenario:
GIVEN a customer of ABC Bakery
WHEN I want to order a pie
THEN I should be able to place the order from home

This is an overall scenario that highlights the actor – which is the customer of the bakery. And the interactions which in case is the urge/intention to order a pie. Then the outcome which is the ability to order a pie online.
This scenario outlines the actions, the trigger (the interaction) and then the outcome. It’s a very high-level requirement as it doesn’t define API endpoints, certain user interface or anything of that nature.
Scenarios needs to always stay with the end-users, the actual customers of the product. And what they do and the outcomes they expect out of the software.
Scenarios sometimes can hand-over to each other. The above scenario is a high-level scenario that can be followed by this scenario here:

GIVEN a customer of ABC Bakery
WHEN I order a pie online
THEN I should receive it within 5 minutes timeframe

This scenario here added up on top of the previous one. It’s already established that customers can order online. Now we have a new scenario that is marketable to everyone where we can say: “We deliver our pies in less than 5 minutes guaranteed!”
Think about your outcomes as something that can be advertised on TV for everyone including non-technical people. What do they care about in terms of outcomes? That’s where these scenarios live.

Here’s a bunch of other examples for reference:

GIVEN a cooker of ABC Bakery
WHEN I need to see pending orders
THEN I should be able to view all my pending orders

GIVEN a manager of ABC Bakery
WHEN I need to monitor the progress of my business
THEN I should be able to see all activity of my business 

The overall theme here is generic overall results. The cooker wants to be able to view all the incoming pending orders. The manager wants to see all activities on the business. Nothing technical or specific to how this is going to be implemented.
More details are welcomed at this level. Scenarios are written in face-to-face meetings with customers. They are raw requirements not yet broken down into features, stories or tasks.
