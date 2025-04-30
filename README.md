# Simulating Network Attacks then Detecting them using Wireshark


<h2>Project Details</h2>
This lab focuses on using Wireshark, a powerful network protocol analyzer, to simulate and detect various network attacks. The hands-on experience was designed to enhance my skills in network security analysis by providing a safe, pre-configured environment to practice detecting malicious activities.<br />
<br />

**Tasks Breakdown:**

**Task 1: Getting Started in the Lab Environment**

Started by initializing the lab environment, which involved setting up the necessary infrastructure. This foundational step ensures that all tools and applications, including Wireshark and the Attack Application, are ready for use.

**Task 2: Using the Attack Application (PS ATTACK ENGINE)**

Learned how to use the Attack Application: PS ATTACK ENGINE (Network TTPs) to simulate different types of network attacks. This is crucial for generating the network traffic needed for analysis.

**Task 3: Capturing Packets with Wireshark**

Opened Wireshark and selected the appropriate network interface (ens5) to begin capturing live packets. This step is essential for monitoring network traffic in real-time.

**Task 4: Analyzing Network Attacks**

Analyzed and Categorized (Source, Destination, Protocol.. etc) the resulting traffic in Wireshark generated from the previous simulated attacks.

**Task 5: Reporting and Visualizing Findings**

Documented the findings from the packet analysis and created visual representations of the network traffic. This step is critical for summarizing insights and sharing them with relevant stakeholders.

<br />

**Key Takeaways:**

This lab enhanced my technical skills in using Wireshark for real-time network traffic analysis and detecting potential malicious activities. It provided practical experience in simulating network attacks and interpreting captured data, which is crucial for effective cybersecurity defense strategies. The ability to use Wireshark's powerful analysis tools prepares me for advanced network security monitoring and threat detection tasks.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Attack Application: PS ATTACK ENGINE (Network TTPs) Used to simulate various network attacks.</b>
- <b>Wireshark: Utilized for capturing and analyzing network traffic.</b> 
  

<h2>Environments Used </h2>

- <b>Linux Desktop Environment: The project was conducted in a Linux-based environment. This choice emphasizes a commitment to leveraging the powerful, versatile capabilities of Linux for network security tasks.

</b>

<h2>Program walk-through:</h2>

**In this lab, I was acting as a security analyst that is using Splunk to review log data related to the company's web application (buttercupgames).**<br/><br/>

**In Task 1 & 2,** I opened Firefox and went to (http://172.31.24.10:8000), waited for Splunk to load, then logged in with the given credentials. After closing the pop-ups, I clicked Add data, chose Upload from your computer, and selected the tutorialdata.zip file from the lab folder. I set the Host to Segment in path with a value of 1, submitted the upload, and clicked Start Searching to access the data. <br/><br/>

**In Task 3,** I started by running a keyword search for buttercupgames error to find related messages. Then I enabled the clientip field to get more specific data and saw that the IP 87.194.216.51 had the most errors. I clicked on it to run a field-based search. After that, I switched the SPL Editor to Full mode in Preferences to see more detailed suggestions while typing. Finally, I ran a transformational search using sourcetype=access_* status=200 action=purchase | top categoryId to find the most common purchase categories.<br/><br/> 

**After that in Task 4,** I saved the previous transformational search by clicking Save as > Report, gave it the title Most popular categories with a description, and clicked Save. Then I viewed the report, edited the permissions to show it to the App and gave Everyone read access. After that, I went back to the search page, ran a new query for the top 10 client IPs, changed the time range to All time, clicked the Visualization tab, and switched the chart from bar to pie. <br/><br/>

**Finally in task 5,** I started by running a search for purchases using sourcetype=access_* status=200 action=purchase, then added the fields date_mday, date_month, and itemId. After that, I ran a new search to find the most sold items by itemId, switched to the Visualization tab, and changed it to a Column Chart. I saved it to a new dashboard called Top Item Purchases. Then I ran another search for top date_mday, changed it to a Bar Chart, and added it to the same dashboard. Finally, I clicked View Dashboard to see both panels together.
<br/><br/>


<p align="center">
Task 1: Getting Started in the Lab Environment <br/>
<br />
<img src="https://i.imgur.com/LU4vJsl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/RayxGso.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/z5sAusS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/czVBfTl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/t390Vx8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<br />
<br />
Task 2: Uploading Data to Splunk  <br/>
<br />
<img src="https://i.imgur.com/tBUG9CM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/k4Rbsny.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/p4Jac9C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/4O5PwxJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/4ugOS5N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/ragQI34.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/OHODcnr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<br />
<br />
Task 3: Performing Searches in Splunk <br/>
<br />
<img src="https://i.imgur.com/ElF0FYj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/hgMv3oP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/F8Kgihc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/XjngoaY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/5xuxeko.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/F3zMExf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/YgMoFYo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br />
<br />
Task 4: Creating and Sharing Reports in Splunk  <br/>
<br />
<img src="https://i.imgur.com/6GSDBPv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/Aeh8OEW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/zuE3XPx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/ABlgQuE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/c5QLRr9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/HKpWDjH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/fiaX8xR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/D3WNr6q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br />
<br />
Task 5: Creating Dashboards in Splunk  <br/>
<br />
<img src="https://i.imgur.com/76wBj83.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/fXlY8kh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/XbzAJrA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/tEqor2v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/7iUSsm0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/m9N43WV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/q4bt5xH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/kx9pOJ8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/1EyX2Fi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/vJNIJae.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
<img src="https://i.imgur.com/YyM4BHj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>









<br />
<br />

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
