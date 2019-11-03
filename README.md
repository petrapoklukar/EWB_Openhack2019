# EWBFlow
## An open source communication platform making knowledge accessible and organised
The proposed solution for the Engineers Without Borders (EWB) challenge, Openhack 2019.

## Challenge objective
A platform for storing and exchanging information between EWB Sweden and their project beneficiaries that would reduce the
likelihood of abandoned systems that fall into disrepair. For a detailed description, see [ EWB_ChallengeDescription_Openhack2019.pdf](https://github.com/petrapoklukar/EWB_Openhack2019/blob/master/EWB_ChallengeDescription_%20Openhack2019.pdf).

## EWBFlow Platform
### Description
We built a mobile app synced with a web version that leverages existing open source communication platforms and enables an easy communication between engineers and project beneficiaries all over the world. Our mobile app, which we named **EWBFlow**, addresses all the requriements of the EWB challenge:
1. it is available both online and offline (see below for details),
2. it contains a Wiki page, specific to each project, where engineers can upload manuals, maps, sketches or any other kinds of supplementary and teaching material,
3. it contains a support forum, specific to each project, where enginners can ask and answer questions, upload images and videos,
4. it supports chat and video call functionallities, 
5. it contains a global forum for sharing information and insights gained from the past projects categorised by the content.

### Mobile App Demo
Click <a href="https://www.figma.com/proto/IWB6k18ao839QL7eOabGoi/EWBFlow?node-id=7%3A0&scaling=scale-down" target="_blank">here</a> to see around the EWBFlow app.

![Image of the Mobile version](https://github.com/petrapoklukar/EWB_Openhack2019/blob/master/Mobileversion_Example.png)

### Web version
A web version demo is available on the following link: http://ewb.northeurope.cloudapp.azure.com/ewb/. 
- At its core it runs an instance of [Question2Answer](https://www.question2answer.org/) which is an open source Q&A platform. It provides a simple way to maintain a knowledge sharing community where users can ask or answer questions. It enables categorization of questions by content using tags, and separately sorts the unanswered questions. Users can also upload images and videos as well as vote on the comments. 
- We added a Wiki page to the forum where engineers can upload any kind of teaching material specific to each project. 
- We also implemented an instance of [Conversejs](https://conversejs.org/) which is a free and open-source XMPP chat client. This feature enables users to get into direct contact with other engineers.  

![Image of the Web version](https://github.com/petrapoklukar/EWB_Openhack2019/blob/master/Webverison_Example.png)

### Technical Details
- The EWBFlow platform is an Ubuntu instance running on a [Microsoft Azure server](https://azure.microsoft.com/en-us/). The estimated cost for EWB to use Azure Virtual MAchine would be ~50$ per month but any other cloud service provider could be used instead. The virtual machine includes the database for storing all the user and project information. 
- The Web server is [Apache2](https://httpd.apache.org/).
- The XMPP chat server is [Prosody IM](https://prosody.im/).
- The chat client is [Conversejs](https://conversejs.org/) 
- The q&a forum is [Question2Answer](https://www.question2answer.org/)
- The mobile version is a wrapper of the web one and it can be used offline. It syncs with the latest web version when the user connects to the internet.

### Challenges and how to overcome them
- *People having troubles to cope with technology (but assuming access to a smartphone)* We would provide an app tutorial showing a new user how to navigate around, potentially in several languages. 
- *Collecting feedback from project beneficiaries and preventing them to abandon the installed system* We would implement a report page where a local engineer could keep track of the system maintaince and log the common issues. This is beneficial for the international engineers as it provides insights on the expected issues and improving the training for the future projects. It could also serve as a way of engaging locals to keep the installed systems alive and rewarding them financially based on the reported health of their system.

### Team 
Made in Stockholm during Openhack 2019 by 
* Anukriti Banerjee
* Björn Bergstrand 
* Muriel Max
* Petra Poklukar
