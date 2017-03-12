![ga](https://cloud.githubusercontent.com/assets/20629455/23824362/2c9817c2-066d-11e7-8988-7b1eefc6d628.jpg)
![wdi](https://cloud.githubusercontent.com/assets/20629455/23824363/2ddeaa7e-066d-11e7-8630-f7c890c9f1c1.png)

___
<br>

#Project 3 | CodeFund

##Overview
For our third project at GA, and our first group project, we were tasked with creating a MEAN stack app. We decided to improve upon Stack Overflow, by incorporating a charity-giving aspect to the operation.

See the app in action here. (ADD LINK).

##The Idea
We decided to create a coding resource app, inspired by Stack Overflow, with an additional charity giving element. Implementing the JustGiving API, users select the charity they'd like donations to be made on their behalf. Users with questions can then post their coding queries to the app, and users with answers can suggest their solutions. Once the person posting the question is satisfied with a respose, he can select it as the 'chosen' one and then donate money to the question respondent's charity.

##The Build
* Back-end: Express/Node
* Database: MongoDB
* Front-end: AngularJS
* CSS framework: Bootstrap
* External API: JustGiving
* Angular modules:
	* Simple HTTP requests: ngResource
	* Authentication: angular-jwt
	* Text editor: textAngular

##The Process
This was the first time we were required to work in a team, so our first task was to get everyone on the same page. After everyone was happy with the idea for the app, we took over a day and a half to hash out how the app would work, how the models would function together, the overall look of the app and who would take on which task, which we then noted in Trello. Once we had planned out as much as possible, we then broke up into our programmings pairs and began the work.

Unsurprisingly, the models proved to be the most difficult portion of this project. Because we knew we wanted to filter the questions by coding language, we decided we would require four models - user, language, question, and answer. The user model would store the basic authentication information, along with the charity selected by the user, and the questions he asked. The language model stored the languages, which were seeded in, and the questions associated with each language. The question models stored the obvious information, plus the moniteary value the question asker would donate in return for a solution. Finally, the answer model stored the response, the owner, the question and whether it was the chosen solution by the question asker, as a Boolean value set to default false.

Concurrently to half the team working on the models, the other half of the team worked on building out the AngularJS authentication.

###Registration view
Here the user supplies his profile information, email and password. This is also where, using the JustGiving API, the user selects the charity he wishes to support. To make it easy, we created a function where the user could type in a charitable interest and then our app would send the search to the API, which would return up to five charities to select from. This information would then be stored in the user model.

###User index view
Once a user registers or logs into the app, he is taken to the user index page, which displays all the registered users.

###User show view
Here, the user can find out more about an individual user, including which charity she supports and any questions she has posted.

###Language index view and language show view
If a user wants to see the various questions asked per language, he must go to the language index page to select the language. This then takes him to a list of all the questions.

###Question new view
Here, the user can post his question, including the incentive he wishes to offer. Using textAngular on this page allows the user to directly type in his question and also to preserve the format of any code he wishes to include. 

###Question show page
The question show page lists the question and a blank box, created using textAngular, where other users can submit their answers, again preserving the format of any code supplied. This is also the page where the user posting the question can select the answer he found most helpful. Once he has done this, a model pops up on the page to inform him how much and to which charity he should donate money to.

##My contribution
For this project, my main responsibilities included:

* keeping the team on track using our Trello boards
* building the models
* building the AngularJS routes
* implementing the JustGiving API into the register process
* creating and collaborating on various views
* styling and branding

##Key Challenges / Learnings
- The biggest challenge on this project was working with four other people who had different strengths, weaknesses and ideas regarding the final product. Overall, I am very happy to have worked as a team on this project, as it taught me a lot about collaborating with other people on code and making decisions, and often, comprimisses. The result, however, was well worth any struggles. Plus, the wins were way more fun!

- As the backbone of the project, we knew we had to have good models to make this a success. Figuring out how many models we'd need, how to have them interact and what information to store was a good challege made harder (and easier) by working in a group.

- This was also the first project we used AngularJS. This was great for the overall result but it was difficult to wrap my head around the framework under the time pressure of this assignment.

- 

##Future work
