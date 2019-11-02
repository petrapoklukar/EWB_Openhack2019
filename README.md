# EWB_Openhack2019
A communication platform for Engineers Without Borders (EWB) Openhack 2019 challenge.

## Challenge objective
A platform for storing and exchanging information between EWB Sweden and their project beneficiaries that would reduce the
likelihood of abandoned systems that fall into disrepair. For a detailed description, see [ EWB_ChallengeDescription_Openhack2019.pdf](https://github.com/petrapoklukar/EWB_Openhack2019/blob/master/EWB_ChallengeDescription_%20Openhack2019.pdf).

## Our Solution: EWBFlow
### Description
We built a mobile app synced with a browser version that leverages existing open source communication platforms. Our mobile app, which we named **EWBFlow**, addresses all the requriements of the EWB challenge:
1. it is available both online and offline, where syncing happens when the user connects to the internet,
2. it contains a Wiki page, specific to each project, where engineers can upload manuals, maps, sketches or any other kinds of supplementary and teaching material,
3. it contains a support forum, specific to each project, where enginners (both local as well as the remote ones) can ask and answer questions, upload images and videos,
4. it supports chat and video call functionallities, 
5. it contains a global forum for sharing information and insights gained from the past projects categorised by the content.

### Mobile App Demo
Here you can click around the EWBFlow app 

### Web Demo
A web version demo is available on this link: http://40.115.118.1/ewb/. At its core it runs an instance of [Question2Answer](https://www.question2answer.org/) which is an open source Q&A platform. It provides a simple way to maintain a knowledge sharing community where users can ask or answer questions. It enables categorization of questions by content using tags, and separately sorts the unanswered questions. Users can also upload images and videos as well as vote on the comments. 

We implemented a [Wiki page](https://github.com/NoahY/q2a-wiki) plugin where engineers can upload any kind of teaching material specific to each project.

We also added an instance of [Conversejs](https://conversejs.org/) which is a free and open-source XMPP chat client. This feature enables users to get into direct contact with other engineers.  

### Technical Details


### Team 
Made in Stockholm during Openhack 2019 by 
* Anukriti Banerjee, 
* Björn Bergstrand, 
* Muriel Max and 
* Petra Poklukar.
