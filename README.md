# 2022-ITCS371-2-Gluay

<h2>Introduction</h2>

<h2>Functional requirements</h2>
<ol>
  <li>They want a website</li>
  <li>The website must have a dog management system.</li>
  <li>The website must have a dog adoption page.</li>
  <li>The website should open 24/7.</li>
  <li>The website must handle like a thousand transactions acrossing a day.</li>
  <li>They want the theme of the organization website to be blue and white.</li>
  <li>The system must ensure no adoption list on the dog that is already adopted.</li>
  <li>The adopter must authenticate their background.</li>
  <li>They want us to prepare the system to handle the security aspect.</li>
  <li>The website must have every treatment record including recording the practicing program.</li>
  <li>The system must handle a delivery option on the website.</li>
  <li>The system must have a sponsor registration process.</li>
  <li>Administrator can see the report of the system(number of the dog available).</li>
  <li>The sponsors can login to the system to manage their brand manner.</li>
  <li>The system must show the sponsor manner on the website.</li>
</ol>

<h2>Non-Functional requirements</h2>
<ol>
  <li>The website must be easy to use for any kind of user.</li>
  <li>The website must have a lot of accessibility.</li>
  <li>The design should be like the same style as the theme.</li>
  <li>The adopter can upload the picture of the dog on the website.</li>
  <li>High resolution picture of the dog on the website.</li>
  <li>The dog’s special list (Fake dead, rolling around) will appear on the website.</li>
  <li>The adopter can see the breed of the dog through a website.</li>
  <li>The adopter can mark the favorite dog to adopt from the dog list.</li>
  <li>The adopter can inform or request to adopt these pets on the website.</li>
  <li>The system has a scheduling of delivery.</li>
</ol>

<h2>Work breakdown structure (WBS)</h2>

<h2>Actors</h2>

|      Actors      |                         Roles                         |                                 
| :--------: | :----------------------------------------------------------: | 
|  **Thai Citizen**   | Thai Citizens can use the services via the website. They are required to authenticate themselves before using the website. They can mark their favorite dog to adopt from the dog list. And request to adopt it. |                                                                                                    
|  **Organization Staff**   |  Organization staff need to record the dog information into the system since the first day that dog arrived. They are also required to record every dog treatment including recording the practicing program. They need to authenticate the adopter before adopting the dog. They will select the adopter to adopt the dog in case that has many adopters to adopt the dog.  |                                                                                                     
| **Admin Staff** |                           Admin staff can view the basic report                            |
| **Eligible Sponsor** | Eligible Sponsors require to register before login to the system to manage their brand manner. |
| **Police Criminal Record Service** | Helps confirm the profile of the adopter by sending back their criminal record. |
| **Blacklist NGO Database Service** | Helps confirm the profile of the adopter by sending back their blacklist status. |

<h2>Functional Decomposition</h2>
<img src="./img/Functional Decomposition.png"></img>

<h2>Use case diagram</h2>
<img src="./img/Detailed Use Case Diagram.png"></img>

<h2>Use case narrative</h2>
<h3>Use case 1 : Dog Profile Management </h3>

|      <b>Use Case Name</b>      |                         <b>Dog Profile Management</b>                         |                                 
| :-------- | :---------------------------------------------------------- | 
|  **Goal in Context**   | Register dog information in to the system |                                                                                                    
|  **Primary Actor**   |  Organization Staff  |                                                                                                     
| **Secondary Actor** |  -  |
| **Precondition** | The Dog is found and available for Register |
| **Trigger** | When the dog is handed to the Organization / Organization staff find the dog that have no owner |
| **Sceneario** | <ol><li>Organization staff login to the website.</li><li>System check username and password.</li><li>If the dog once registered in other organization before, get the dog data from that organization.</li><li>Organization staff input the dog breed,health information,color,medical record,blood group etc of that dog into the dog profile on the system.</li><li>The system creates a new dog profile in association with the information that  organization staff put in.</li><li>Organization staff bring the dog to the next process.</li></ol>|
| **Exceptions** | <ol><li>Exception 1. If The dog already registered to the system before,The system will ask you to update the old profile</li> <li>Exception 2. If Someone adopt the dog physically before the process is done, Rollback the dog profile in the system.</li></ol> |
| **Post-condition** | Dog profile will be shown in the website. |

<h3>Use case 2 : Adopting Dog </h3>

|      <b>Use Case Name</b>      |                         <b>Adopting Dog</b>                         |                                 
| :-------- | :---------------------------------------------------------- | 
|  **Goal in Context**   | Thai Citizen attempt to adopt a dog |                                                                                                    
|  **Primary Actor**   |  Thai Citizen  |                                                                                                     
| **Secondary Actor** |  Organization Staff  |
| **Precondition** | Thai Citizen must pass the verification process |
| **Trigger** | Thai Citizen want to adopt the dog |
| **Sceneario** | <ol><li>Thai Citizen login to organization website</li><li>System check username and password.</li><li>System check for user adoption verification from organization database.</li><li>Thai Citizen selected the dog that they want from the system</li><li>Thai Citizen send requests to adopt the dog that they choose with Short essay and their Citizen ID</li><li>System sends information to Organization staff for approval.</li></ol>|
| **Exceptions** | <ol><li>Exception 1. If the Thai Citizen do not have an account to log on, see use case register</li><li>Exception 2. If the user name and password are incorrect, system will prompt to Thai Citizen to retry log on </li><li>Exception 3. If the Thai Citizen doesn't complete the short essay or submit the blank paper ,The system will notify the Thai Citizen to resubmit the essay</li></ol> |
| **Post-condition** | The dog adoption request will sent to the organization staff |

<h2>Data flow diagram Level 0</h2>
<img src="./img/DFD LV0.png"></img>
