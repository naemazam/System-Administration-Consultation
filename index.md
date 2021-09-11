
|Due Oct 11, 12:59 PM +06|
|Naem Azam|

|System Administration Consultation|

|Question1.|
| |
|Learning Goals:Use the systems administration concepts you learned in the course to provide technical improvements to current processes.|
| |
|Implement solutions based on an organization’s restrictions, like financial resources, number of users, etc.|
|Overview: You’ll take what you learned in the System Administration and IT Infrastructure Services course and apply that knowledge to real-world situations.|
|Assignment: For this writing project, you’ll be presented with three scenarios for different companies. You’ll be doing the systems administration for each company’s IT infrastructure. For each scenario, present improvements to processes based on the company’s needs and current restrictions. There’s no right or wrong answer to your consultation, but your responses should explain the problem, the improvement, and the rationale behind them. Please write a 200-400 word process review for each company presented to you.|
| |
|Scenario 1: |
|You’re doing systems administration work for Network Funtime Company. Evaluate their current IT infrastructure needs and limitations, then provide at least five process improvements and rationale behind those improvements. Write a 200-400 word process review for this consultation. Remember, there’s no right or wrong answer, but make sure to provide your reasoning.|
|Software Company:|
|Network Funtime Company is a small company that builds open-source software. The company is made up software engineers, a few designers, one person in Human Resources (HR), and a small sales team. Altogether, there are 100 employees. They recently hired you as a system administrator to come in and become their IT department.|
|When a new person is hired on, the HR person purchases a laptop for them to do their work. The HR representative is unfamiliar with what type of hardware is out there; if a new employee requests a laptop, the HR person will purchase the cheapest option for a laptop online. Because of this, almost everyone has a different laptop model. The company doesn’t have too much revenue to spend, so they don’t order laptops until someone gets hired at the company. This leads to a few days of wait time from when someone starts to when they can actually work on a laptop.The company doesn’t label their computers with anything, so if a computer is missing or stolen, there’s no way to audit it. There’s no inventory system to keep track of what’s currently in the fleet.Once a computer is purchased, the HR person hands it to the new employee to set up. Software engineers that use Linux have to find a USB drive and add their preferred distribution to the laptop. Anytime someone needs something from HR -- whether it’s office related or tech related -- they email the HR representative directly.When a new employee gets a machine, they’re given logins to use cloud services. They get a personal orientation with HR to make sure they can login. This requires the HR person to block off a few hours for every new employee. If an employee forgets the login to their machine, they have no way to retrieve a password and they have to reimagine their machine. Employees don’t have a strict password requirement to set for their computers.The company currently has many of their services in the cloud, such as email, word processors, spreadsheet applications, etc. They also use the application, Slack, for instant communication.|

|Answer|
|This company is in desperate need of infrastructure management.First, purchasing computers from the internet when they are needed is a very inefficient process. This results in lost time and productivity. In a company this size, having at least three spare laptops ready to go into service would help everyone, especially in emergencies. Also, buying the cheapest laptop is always a bad idea. Company assets need to be documented and inventoried, including all computers, printers, and networking gear.Even if the entire company only uses cloud services, I think they would benefit from having a domain controller and some kind of central management service, such as OpenLDAP to track computers connected to the domain. This could be used to provision software to any computers joined to the domain, and would implement some kind of strict password management.This company is large enough to justify the time and expense to set this up.|


|Correct|
| |
|Thank you for your submission!|
|An excellent response|
| |
|explains the problem or restrictions that the company faces in great detail.|
| |
|lists five or more process improvements and explains how they plan to implement each of them.|
| |
|thoroughly explains the rationale behind each improvement recommendation.|
|2.|
| |


|Scenario 2:|
|You’re doing systems administration work for W.D. Widgets. Evaluate their current IT infrastructure needs and limitations, then provide at least five process improvements and rationale behind those improvements. Please write a 200-400 word process review for this consultation. Remember, there’s no right or wrong answer, but make sure to provide your reasoning.|
|Sales Company:W.D. Widgets is a small company that sells widgets. They’re mostly made up of salespeople who work with lots of clients. You’ve taken over as the sole IT person for this company of 80-100 people.When HR tells you to provision a machine for a new employee, you order the hardware directly from a business vendor. You keep one or two machines in stock, in case of emergency. The users receive a username that you generate for them. You then give them an orientation on how to login when they start. You currently manage all of your machines using Windows Active Directory. The company uses only Windows computers. When a new computer is provisioned, you have to install lots of sales-specific applications manually onto every machine. This takes a few hours of your time for each machine. When someone has an IT-related request, they email you directly to help them.|
|Almost all software is kept in-house, meaning that you’re responsible for the email server, local machine software, and instant messenger. None of the company’s services are kept on the cloud.Customer data is stored on a single file server. When a new salesperson starts, you also map this file server onto their local machine, so that they can access it like a directory. Whoever creates a folder on this server owns that folder and everything in it. There are no backups to this critical customer data. If a user deletes something, it may be lost for everyone.The company generates a lot of revenue and is rapidly growing. They’re expecting to hire hundreds of new employees in the next year or so, and you may not be able to scale your operations at the pace you’re working.|

|Answer|
|This company would probably benefit from setting up GPOs and assigning roles to users. This would allow you to push software out to machines based on what role they have been assigned in Active Directory. This would keep you from having to install the software manually on any new machine.You should be creating backups of the fileserver both locally and through a cloud service. It may also be a good idea to re-assign file permissions and security groups, so that only domain admins have full control of files and directories. All users could be assigned permissions based on roles in the company, and corresponding GPOs.Finally, you should hire an assistant now, before the workload increases beyond what you can handle alone. You may want to hire someone to take on a defined part of the IT responsibilities, such as low-level helpdesk/support tech, or you could hire a “counterpart” who would be able to also do everything that you do.|


|Correct|
| |
|Thank you for your submission!|
|An excellent response|
| |
|explains the problem or restrictions that the company faces in great detail.|
| |
|lists five or more process improvements and explains how they plan to implement each of them.|
| |
|thoroughly explains the rationale behind each improvement recommendation.|


|Question3.|
| |
|You’re doing systems administration work for Dewgood. Evaluate their current IT infrastructure needs and limitations, then provide at least five process improvements and rationale behind those improvements. Please write a 200-400 word process review for this consultation. Remember, there’s no right or wrong answer, but make sure to provide your reasoning.|
|Non-profit Company:Dewgood is a small, local non-profit company of 50 employees. They hired you as the sole IT person in the company. The HR person tells you when they need a new computer for an employee. Currently, computers are purchased directly in a physical store on the day that an employee is hired. This is due to budget reasons, as they can’t keep extra stock in the store.The company has a single server with multiple services on it, a file server, and email. They don’t currently have a messaging system in place. When a new employee is hired, you have to do an orientation with them for login. You’re also responsible for installing all the software they need on their machine, and mapping the file server to their computer. The computers are managed through Windows Active Directory. When an employee leaves, they’re currently not disabled in the directory service.|
|The company uses an open-source ticketing system to handle all internal requests as well as external non-profit requests. But the ticketing system is confusing and difficult to use, so lots of the employees reach out to you directly to figure out how to do things. In fact, so many things are difficult to find that employees typically ask around when they have a question.There are nightly backups in place of the file server. You store this information on a disk backup and take it home with you everyday to keep it safe in case something happens onsite. There’s also a small company website that’s hosted on the single server at the company. This website is a single html page that explains the mission of the company and provides contact information. The website has gone down many times, and no one knows what to do when it happens.|
|Answer|
|I think the most troubling thing about this company is the backup system. Making a disk backup isn’t bad, but someone driving around with it seems like an accident being invited to happen. Make a cloud backup, a disk backup that stays onsite, and a third that the IT person can drive around with.The ticket system should be replaced or the employees should be trained to use it. If it is there, it needs to be in use and effective for people to use.Again, I think this org should reconfigure AD with roles and GPOs for users so that they can have software automatically installed on their machines at login. And the IT person needs to be maintaining accounts and deleting users when they leave the organization.Running the website on your own server, especially for a single HTML page, makes no sense at this time. Pay the $10/year for your page to be hosted by a hosting service and enjoy the 99%+ uptime.|

|Correct|
| |
|Thank you for your submission!|
|An excellent response|
| |
|explains the problem or restrictions that the company faces in great detail.|
| |
|lists five or more process improvements and explains how they plan to implement each of them.|
| |
|thoroughly explains the rationale behind each improvement recommendation.|
