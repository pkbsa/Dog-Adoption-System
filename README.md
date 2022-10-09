# 2022-ITCS371-2-Gluay

<h2>Introduction</h2>

The Dog Adoption management system for nonprofit organizations is similar to what we are going to do so far. Our customers, which are nonprofit organizations, ask us to develop a platform to handle stray dogs. First, it’s the Thai citizens service. People can check our website and services will be provided on the website. They want a platform to adopt stray dogs. The second party is the organization staff, they have to respond for content generated, content generating and input the dog profiles into the platforms. The Third party is admin staff so they are looking for some report from the system. The fourth are the sponsors. You know these are nonprofit organizations, but they still need support.
 
The feature starts from the first one. Dog profile management. The first day that the dog comes under the care of this organization, the staff must register that dog into the system, so the system has to ask for input lay and breach of the dog like a color, some other medical profile so you can check the dog adoption page. Those dogs have to pass practice so we don't want to give the killer dogs to the adopter. We have to treat them well and get some medical treatment. The users will come and can search for a particular type of the dogs or general.
 
According to their criteria, they see the list of the dogs and the picture of the dog and then some special characteristics, the adoption process is not that simple, we must pass some verification process. This verification process involves some external system. First one is a criminal record from the police so we don't want our dogs to fall into the hands of criminals.  After the staff verify that the adoption, they can see the list of the dog, and they can mark the favorite list after they want to make an adoption. If there are so many people interested in adopting this dog. We must do this. It is not first come first serve so the organization's staff will select the most suitable adopter to adopt the dog. The system must also handle the dog delivery as well, so there will be a function of a delivery schedule. The last group is the sponsor that can be the organizations who want to support this dog adoption organization. The sponsor can make a registration, can pass the registration process and then specify that they want to support the organization, and this is a support specification to support the organization, the benefit that the sponsor can get is that the system must can show the brand and logo of the supporter on the website. For the sponsorship the organization provides just one size of brander, no matter how much they support but just only one size of brander that will appear on the website.
 
Regarding some system characteristics, they want this system as a website that is easy to use for any kind of user. The design must be easy enough to use and then you need to also think about the accessibility of the website because some blind people or some color blindness people . The availability of the service should be 24 / 7, they can handle thousands of transactions per day. To enhance the stability of the system, they want us to prepare the system to handle the security aspect. The theme color theme of this organization is blue and white so, our design should be like the same style according to their theme blue and white that is that design. In that first year for the first year every month, the organizations will check whether the dog is still fine is like a checkout process. We have to follow the adoptions for one year and then they do it every month, they will call the adopter and for that the adapter will post a picture or the organization will do some invitations to check whether those dogs are healthier and then we have to record those checkup data as well.


<h2>Functional requirements</h2>
<ol>
  <li>The Organizations want a website</li>
  <li>The website must have a dog management system.</li>
  <li>The website must have a dog adoption page.</li>
  <li>The website should open 24/7.</li>
  <li>The website must handle like a thousand transactions acrossing a day.</li>
  <li>The Organizations want the theme of the organization website to be blue and white.</li>
  <li>The system must ensure no adoption list on the dog that is already adopted.</li>
  <li>The adopter must authenticate their background.</li>
  <li>The Organizations want us to prepare the system to handle the security aspect.</li>
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
<img src="./img/Functional Decomposition.png"></img>

<h2>Actors</h2>

|      Actors      |                         Roles                         |                                 
| :--------: | :----------------------------------------------------------: | 
|  **Thai Citizen**   | Thai Citizens can use the services via the website. They are required to authenticate themselves before using the website. They can mark their favorite dog to adopt from the dog list. And request to adopt it. |                                                                                                    
|  **Organization Staff**   |  Organization staff need to record the dog information into the system since the first day that dog arrived. They are also required to record every dog treatment including recording the practicing program. They need to authenticate the adopter before adopting the dog. They will select the adopter to adopt the dog in case that has many adopters to adopt the dog.  |                                                                                                     
| **Admin Staff** |                           Admin staff can view the basic report                            |
| **Eligible Sponsor** | Eligible Sponsors require to register before login to the system to manage their brand manner. |
| **Police Criminal Record Service** | Helps confirm the profile of the adopter by sending back their criminal record. |
| **Blacklist NGO Database Service** | Helps confirm the profile of the adopter by sending back their blacklist status. |

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
| **Precondition** | Thai Citizen must be login |
| **Trigger** | Thai Citizen want to adopt the dog |
| **Sceneario** | <ol><li>Thai Citizen login to organization website</li><li>System check username and password.</li><li>System check for user adoption verification from organization database.</li><li>Thai Citizen selected the dog that they want from the system</li><li>Thai Citizen send requests to adopt the dog that they choose with Short essay and their Citizen ID</li><li>System sends information to Organization staff for approval.</li></ol>|
| **Exceptions** | <ol><li>Exception 1. If the Thai Citizen do not have an account to log on, see use case register</li><li>Exception 2. If the user name and password are incorrect, system will prompt to Thai Citizen to retry log on </li><li>Exception 3. If the Thai Citizen doesn't complete the short essay or submit the blank paper ,The system will notify the Thai Citizen to resubmit the essay</li></ol> |
| **Post-condition** | The dog adoption request will be sent to the organization staff |

<h3>Use case 3 : Verify Adopter </h3>

|      <b>Use Case Name</b>      |                         <b>Verify Adopter</b>                         |                                 
| :-------- | :---------------------------------------------------------- | 
|  **Goal in Context**   | To make sure that dog will go to live with the best Adopter |                                                                                                    
|  **Primary Actor**   |  Organization Staff  |                                                                                                     
| **Secondary Actor** |  Police Criminal Record Service, Blacklist NGO Database Service  |
| **Precondition** | Thai Citizen must pass the Adopting Dog Process |
| **Trigger** | Thai Citizen send the adoption request to the system |
| **Sceneario** | <ol><li>Thai Citizen send the dog adoption ticket to the system</li><li>System check the adopter criminal record with the Police Criminal Record Service using adopter Citizen ID.</li><li>System check the adopter blacklist status with Blacklist NGO Database Service using adopter Citizen ID.</li><li>The system send the Adopter criminal record, blacklist status, short essay, and general information to the Organization staff</li><li>Staff will send back the approval status to the system</li><li>system will go the the Selecting Adopter process</li></ol>|
| **Exceptions** | <ol><li>Exception 1. If the Police Criminal Record Service is down the system will be rolled back.</li><li>Exception 2. If the Blacklist NGO Database Service is down the system will be rolled back. </li><li>Exception 3. If the adopter Citizen ID is incorrect or provided with false information, The system will prompt the adopter to send a new ticket</li></ol> |
| **Post-condition** | The adopter will be added to the adopter list which will be selected to find the most suitable adopter|

<h3>Use case 4 : Add Supporter Visualization </h3>

|      <b>Use Case Name</b>      |                         <b>Add Supporter Visualization</b>                         |                                 
| :-------- | :---------------------------------------------------------- | 
|  **Goal in Context**   | To add the banner to the Organization Website |                                                                                                    
|  **Primary Actor**   |  Eligible Sponsor  |                                                                                                     
| **Secondary Actor** |  Organization Staff  |
| **Precondition** | The Eligible sponsor must be approved by the Organization Staff |
| **Trigger** | Eligible sponsor want to upload their banner to the website |
| **Sceneario** | <ol><li>Eligible sponsor log on to the website</li><li>System check username ,password and access rights.</li><li>Eligible sponsor upload their banner up to the website</li><li>The system check the banner resolution and update their website</li></ol>|
| **Exceptions** | <ol><li>Exception 1. If the Eligible do not have an account, see use case register</li><li>Exception 2. If the user name and password are incorrect, system will prompt to citizens to retry to log on. </li><li>Exception 3. If the uploaded banner size is in correct or the file is to large, the system will prompt to Eligible sponsor to upload a new file</li></ol> |
| **Post-condition** | The banner is uploaded to the website|


<h2>Data flow diagram Level 0</h2>
<img src="./img/DFD LV0.png"></img>
