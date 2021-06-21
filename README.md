# VaxNotifier
Vaccine Notification System

#Inspiration
The year is 2021, the deathly virus that is COVID-19 continues to plague the world. What better way to stay safe and protect your family from the pandemic than having a vaccination?

However, vaccines don't come easily. Despite the continuous efforts of organizations like VaxHunter Canada at informing the public about available vaccine appointments through Twitter tweets. People often miss the tweets because of the lack of a notification system (VaxHunter also tweets 100+ a day, which is a lot to keep track of!).

With every need, there comes a solution. At TOHacks 2021, we proudly present: VaxNotifier

#What it does
VaxNotifier is a notification system that informs users of available vaccine appointments through an SMS text message.

Step 1 - Registration
The users register on a website that takes their name, phone number, and location. A welcome message is generated by the SMS system and sent to the user to verify his/her identity.

Step 2 - Tweet Checker Algorithm
An algorithm checks VaxHunter Canada's tweets every 10 minutes for new vaccine appointments. If vaccine appointments are detected in the same city as the user, the application proceeds to the next step.

Step 3 - SMS system
After the completion of step 2, a custom SMS text message is sent to the user's phone number, which informs the user of the address of the vaccine appointments mentioned in the original Twitter post.

#How we built it
Webpage
We used Figma to create the design, then used HTML/CSS to create the webpage.

Tweet Checker Algorithm
The Twitter API was used to get the tweets from VaxHunter Canada, important information such as the city where the vaccines are available was parsed out. An algorithm created in Python compares the user's location to the location given in the tweets. A software utility called cron was used to check for new tweets every 10 minutes.

Courier SMS system
We used Courier to send the SMS text. A customized SMS text was created in the Courier app. A python program was created using Courier's Python SDK to create/modify the user's profile in the courier database and send the SMS message.

#Challenges we ran into
Trying to implement Courier proved to be challenging, as there were a number of commands that we did not fully understand. Thankfully, with the support of Courier's sponsor team and API documentation, we were able to successfully implement the code.

#Accomplishments that we're proud of
Being able to use the Courier API to send and receive messages in Python. We were very proud that we got it to work after many failed attempts. Also, we were really impressed to see how the front end, back end, and Courier API, which were handled by different people, were able to come together in the end.

#What we learned
Data scraping using the Twitter API.
Gained experience in software development and workflow.
Knowledge of the Courier API & Figma.
#What's next for VaxNotifier
As the next steps, we look forward to finding ways to refine our program and bring our services to the next level. We will aim to implement code to display the nearest clinic and distance from the user's address. That way, the user is able to get a better sense of the vaccine's location and make a more informed decision about whether or not to go to the clinic.
