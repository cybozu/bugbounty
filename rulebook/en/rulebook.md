Cybozu Bug Bounty Program Rulebook
===
# 0. Preface
The Cybozu Bug Bounty Program (hereafter called "this program") is a system intended to early discover and remove zero-day vulnerabilities that might exist in services provided by Cybozu. Under this program, people who discover vulnerabilities and report them to us (hereafter called "reporters") will be paid a reward as a token of our gratitude for cooperating to help us improve the quality of our services.  
In the event of any discrepancies between the Japanese version and the English version, the Japanese version shall prevail.

# 1. Services That Are Applicable for Testing
Please refer to the following page for the services that are subject to testing under this program. [https://cybozu.co.jp/products/bug-bounty/en/](https://cybozu.co.jp/products/bug-bounty/)  
The latest versions of each service are covered by this program. To learn the details about our services, refer to the Web site of each product.

# 2. Terms and Conditions on Reporting
Those who fulfill all conditions below can earn a reward for reporting vulnerability information under this program.
- You are not an employee of Cybozu or its subsidiary companies as of the time of reporting.
- You do not work for Cybozu or its subsidiary companies as of the time of reporting under a contract such as a work delegation agreement, secondment agreement, dispatching agreement or the like.
- Within the one year prior to the reporting date, you were not a regular fulltime employee of Cybozu or its subsidiary companies.
- Within the one year prior to the reporting date, you were not engaged in the product development and cloud service operation related tasks at Cybozu or its subsidiary companies.
- You can communicate with Cy-PSIRT in Japanese or English.
- You agree with the Terms and Conditions for Cybozu Bug Bounty Program.

You can find the Terms and Conditions for Cybozu Bug Bounty Program at the following URL:  
https://cybozu.co.jp/products/bug-bounty/pdf/terms.pdf

# 3. Communication
## 3.1 Contact Us
This program is managed by Cy-PSIRT under Cybozu, Inc.  
Through the reporting site, you can contact us with your question about reporting vulnerabilities under this program. If you do not have an account of the reporting site, please apply it from the reporting site account request form.  

Reporting Site:  
https://cy-bugbounty.cybozu.com/k/  
Reporting Site Account Request Form:  
https://cy-psirt.form.kintoneapp.com/public/d16726f3de2ce25f846c43603fe7260c80a5adbc1ed878a7fcd66f8b671be525   

As for other questions, you can also contact us at our e-mail address.  
E-mail:  
productsecurity@cybozu.co.jp

## 3.2 PGP Key
When reporters contact Cy-PSIRT, they can use a PGP key. The public key information is available at the following:  
https://www.cybozu.com/jp/features/management/cy-psirt.asc

# 4. Cybozu Vulnerability Information Handling Policy
All vulnerability information that is reported to Cybozu will be received and handled in accordance with Cybozu's "Vulnerability Information Handling Policy". The Vulnerability Information Handling Policy defines how we will handle and publicize any vulnerabilities that are discovered in the products and services that Cybozu offers. For details, refer to the following Japanese Web site:  
https://cybozu.co.jp/company/security-policy/

# 5. Response Process for Vulnerability Information
## 5.1 Response Process
A vulnerability reported from a reporter to Cy-PSIRT is evaluated by using the following process:

1. Cy-PSIRT assigns a "response number" and communicate it to the reporter.
2. Cy-PSIRT decides whether to identify the report as a vulnerability (\*1) based on the reported information. When it is identified as a vulnerability, Cy-PSIRT also calculates the reward amount.
3. Cy-PSIRT contacts the reporter with the evaluation results.
4. The reporter contacts Cy-PSIRT with "response completed", and then the response process is completed. (\*2)  

\*1 The term "identify" means that we recognize the behavior in the services subject to the Program as a vulnerability qualified for a reward, and the date we recognize it as a vulnerability is referred to as the identified date. If the necessary information is not provided to identify the reported information as a vulnerability, we may contact the reporter to provide the additional information.  
\*2 When Cy-PSIRT notifies a result of the investigation, we mention the reply due date. Even if we do not receive a reply from the reporter by the due date, the response process is also treated as completed.

At the time of notifying the reporter of the result, the evaluation and the payment amount may vary.  
When the response process is completed, the amount of the reward is determined and the payment amount is not changed thereafter.

## 5.2 Order in Which Inquiries to Be Accepted
As for received inquiries, we accept them in the order of receipt.

## 5.3 Support Hours
We receive vulnerability reports and inquiries from 10:00 a.m. to 5:00 p.m. (JST) on weekdays.  
Generally, received reports and inquiries are accepted within three business days.  
Please note that it may take longer than usual due to our non-working days such as the year-end and New Year holidays.

## 5.4 Order in Which Vulnerabilities to Be Evaluated
Generally, vulnerabilities are evaluated in the order of the "response number". However, the evaluation order may be changed due to the vulnerability report status and so on.

# 6. Rewards
## 6.1 Payment Amount
The amount of the reward is determined according to the following rules:  
The reward amount to be paid is doubled if the option to donate is selected. For details, refer to "6.4 Donating Rewards".

### Products and Services
||kintone(\*1)<br>cybozu.com Administration(\*1)<br> cybozu.com Store<br>Marketplace|Garoon(\*1)<br>Mailwise<br>Office|cybozu.com operational base<br>Client Certificate Authentication<br>Cybozu Desktop 2 (for Windows)|
|:--|:--|:--|:--|
|RCE|2,000,000 Japanese Yen (Fixed)|2,000,000 Japanese Yen (Fixed)|2,000,000 Japanese Yen (Fixed)|
|SQL injection|400,000 to 1,600,000 Japanese Yen|100,000 to 1,000,000 Japanese Yen||
|XSS|100,000 to 400,000 Japanese Yen|50,000 to 200,000 Japanese Yen||
|Injection (other than SQL injection)|50,000 to 350,000 Japanese Yen|40,000 to 200,000 Japanese Yen||
|Deficiency in access control|200,000 to 800,000 Japanese Yen|50,000 to 400,000 Japanese Yen||
|Vulnerability specific in a mobile app|10,000 to 2,000,000 Japanese Yen<br>(Scope: kintone Mobile)|10,000 to 2,000,000 Japanese Yen<br>(Scope: Cloud edition Garoon Mobile, Cybozu Office Mobile)||
|Others|10,000 to 2,000,000 Japanese Yen|10,000 to 2,000,000 Japanese Yen|10,000 to 2,000,000 Japanese Yen|

(\*1) including APIs integrated in each product


### Web sites
|No.|Summary|Case|Amount|
|--|--|--|--|
|1|RCE or not|RCE|1,000,000 Japanese Yen (Fixed)|
|||Other than RCE|20,000 Japanese Yen (Fixed)|

For the list of applicable Web sites under this program, refer to "Applicable Products, Services, and Web Sites" mentioned below.  
https://cybozu.co.jp/products/bug-bounty/

## 6.2 Supplementary Rules on Earing Rewards
|No.|Summary|Rules|
|--|--|--|
|1|As a result of investigation, multiple qualifying vulnerabilities are identified.|If a reporter submits multiple vulnerability reports, the reporter can earn corresponding reward for them. However, the reporter cannot earn reward for vulnerabilities that Cy-PSIRT detects in the identical product or other products as a result of investigation based on the reported information.|
|2|Vulnerabilities with the same root cause are reported.|When we receive multiple reports of vulnerabilities with the same root cause in the identical product, the first reported vulnerability information is identified as a qualifying vulnerability. Only the reporter of the identified vulnerability can earn a reward.|
|3|A known vulnerability is reported.|If a reported vulnerability is the vulnerability that we have already recognized, the reporter cannot earn a reward.|
|4|A vulnerability is reported for an environment that is not supported. |If a reported vulnerability is reproduced in an environment that is not supported, the reporter cannot earn a reward. For information about supported environments, refer to the Web site of each product.
|5|As a result of investigation, the evaluation results are changed.|If the evaluation results are changed as a result of our investigation, the reward amount will also be changed according to the changed score only on the condition that the response process is not completed.|

### 6.2.1 Examples of Identical Vulnerabilities with the Same Root Cause
- Both input from a parameter and input from a hash object expose vulnerabilities.
- Multiple Web sites hosted on the same server expose vulnerabilities caused by the configuration of the environment.
- Different programs in the identical product use the identical logic, function, and so forth, and thus they expose vulnerabilities.

These rules do not apply if vulnerabilities with the same root cause are exposed in different products.

### 6.2.2 Reports That Are Not Eligible for Rewards
If a report meets any of the following criteria, we are generally unable to identify the report and provide payment for rewards.  
1. Reports that include vulnerabilities listed in “What Are NOT Identified as Vulnerabilities” of [Vulnerability Identification Guidelines](https://github.com/cybozu/bugbounty/tree/master/guideline/en)
2. Reports in which the specific threat or the service being reported is unknown (For example: a report in which output results from an automated program to scan vulnerabilities are simply pasted)

However, even if a report meets the criterion 1 above, the report may be eligible for rewards, provided that we recognize the report as a crucial one. 

## 6.3 Delivery of Rewards

We transfer the reward in cash at the end of the second month after the completion of our response process.  
Reporters must send their bank details to Cy-PSIRT. Please check the Terms and Conditions as for the list of banks you can designate.  
The payment may take a long time or fail to be completed (a) if we do not receive bank details or (b) even if we make a bank transfer according to the provided bank details but the reporter cannot receive the reward.

## 6.4 Donating Rewards
Reporters can donate earned reward to an OSS community selected by us, instead of claiming the reward. If reporters choose to donate their reward, Cybozu also will donate the same amount as their reward to the OSS community. However, you must accept each reward in its entirety or donate it. You cannot split the reward between yourself and a donation.

### 6.4.1 Donation Recipients Selected by Cybozu
- Apache Software Foundation 
- Linux Foundation
- OWASP Local Chapter in Japan

If a reporter does not specify a recipient, we make the donation to the Apache Software Foundation.

### 6.4.2 Donation Details
Once we have been contacted by a reporter saying that they wish to donate, Cybozu makes the donation to the organization of the reporter's choice. The donation is made in the name of "Cybozu, Inc."  
Once the donation has been made, Cy-PSIRT notifies the reporter of the completion.  
We cannot accept requests such as issuing documents intended to be used for tax breaks, and so on. It is confirmed that the recipients listed above cannot enable a reporter to receive a tax break when the reporter lives in Japan.

## 6.5 Taxation
Reporters who have earned reward may be required to file a tax declaration in accordance with the laws of their country.  
Taxation systems differ from country to country. Please check the system by yourself and take necessary actions.  
We do not issue payment records, because reporters do not need to attach payment records to their final tax return forms in the case of Japan.  

# 7. Points

## 7.1 Calculation of Points to Be Given

In addition to reward, reporters can earn points depending on their reports.  
The following are points for reference, and we decide the actual number of points.  
In addition to the points specified below, points are given depending on the situation, such as when we recognize the report as the practical information.  

### 7.1.1 Earning Basic Points by Reporting

|No.| Case| Details | Points|
|--|--|--|--|
|1| Vulnerability of product/service (excluding RCE)|A vulnerability of product or service is reported.| 10 to 40 |
| | Vulnerability of Web site (excluding RCE) | A vulnerability of Web site is reported.<br>\* Formulas 2 to 3 are not applied. |10|
| |RCE|An RCE is reported.|40|
|2| Accuracy of reproduction methods|We determine the number of points based on reported information.|0 or 10|
3|Clear description of the impact|We determine the number of points based on reported information.|0 or 10|
|4|Impact on cybozu.com operational base|A vulnerability which gives an impact on "cybozu.com operational base" is reported.|10|
|5|Cybozu award|We comprehensively evaluate reports for their severity for Cybozu, urgency, impact, and others and then, once a year, decide which reports we give the award to.<br>\* The points are given when the decision is made. Also, points are given for each awarded report. We may also award multiple reports.|100|

In addition to reporting, we may also give points for activities such as attending events and achieving test results.

### 7.1.2 Ranks and Multipliers

We set some ranks based on the testing and reporting performance in the past. Reporters are eligible for earning points, which are calculated by multiplying the basic points by the multiplier set for each rank.

|Rank Name|Rank Conditions|Multiplier|
|--|--|--|
|Platinum|Fulfill all conditions below<br>The number of reports in the last one year is 20 or more<br>The sum of basic points earned in the last one year is 400 points or more|2.0|
|Gold|Fulfill all conditions below<br>The number of reports in the last one year is 10 or more<br>The sum of basic points earned in the last one year is 200 points or more|1.8|
|Silver|Fulfill all conditions below<br>The number of reports in the last one year is 1 or more<br>The average number of accesses to the testing environment in the last three months is 100 or more|1.5|
|Bronze|Others|1.0|

Ranks are changed based on information as of the end of each month, and new ranks become effective around the beginning of the following month. Regardless of the submitted date of the report, rank multipliers when the points are given are applied.  


## 7.2 Benefits to Be Given for the Points

Reporters can redeem their points for a corresponding prize which can be selected from the list we provide.  
Reporters who want to redeem their points must send their mailing address information to Cy-PSIRT. We start the delivery process after we receive the mailing address.  
Please note that, depending on the delivery destination, delivery may take some time or we may not be able to send a requested gift.  
Furthermore, reporters may be required to submit a final income tax return depending on a prize for which they have redeemed their points. In such cases, articles in "6.5 Taxation" also apply.

## 7.3 Real-Time Point Ranking

The ranking of the earned points is published, such as on our social networking sites.  
Reporters can specify their display name in the ranking, or can choose to be anonymous.

## 7.4 Others

- Earned points expire either at the end of the month when an account of the reporting site is deleted or at the end of three years after they have been earned, and cannot be used thereafter.
- This point system is subject to change in accordance with "9. Amendment of Rulebook". The point system may also be suspended or terminated for our operational reasons. In the case of suspension or termination, we will provide the relevant information for an appropriate time period and in an appropriate manner, in light of the impact of the suspension or termination and the status of the operation of this point system.

# 8. Acknowledgments
Names of reporters who find and report vulnerabilities based on this program will be listed on the "Special thanks to contributors who have enhanced our service quality" page in token of our gratitude. Please refer to the following page for the details on who can receive the acknowledgement and when contributors are listed.
https://cybozu.co.jp/products/bug-bounty/specialthanks/

# 9. Amendment of Rulebook
Cybozu shall be entitled to amend this Rulebook without prior public notification.
When amending a key portion of this Rulebook, Cybozu shall provide the participants with notice of the details thereof.  

# 10. Testing Environment
Refer to the Bug Bounty Testing Environment Program page.
https://cybozu.co.jp/products/bug-bounty/#TestingEnvironmentProgram
