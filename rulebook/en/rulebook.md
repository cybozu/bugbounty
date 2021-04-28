Cybozu Bug Bounty Program Rulebook
===

# 0. Preface
The Cybozu Bug Bounty Program (hereafter called "this program") is a system intended to early discover and remove zero-day vulnerabilities that might exist in services provided by Cybozu. Under this program, people who discover vulnerabilities and report them to us (hereafter called "reporters") will be paid a reward as a token of our gratitude for cooperating to help us improve the quality of our services.  
For the details of the program period, please refer to the Cybozu Bug Bounty Program page (https://cybozu.co.jp/products/bug-bounty/).


# 1. Services That Are Applicable for Testing
To learn which services are applicable for testing under this program, see the Cybozu Bug Bounty Program page ([https://cybozu.co.jp/products/bug-bounty/en/](https://cybozu.co.jp/products/bug-bounty/en/)). The latest versions of each service are the targets of testing under this program. To learn the details about our services, see the Web site of each product.

# 2. Terms and Conditions on Reporting
Those who fulfill the below conditions may receive a reward for reporting vulnerability information under this program.

- You are not an employee of Cybozu or its subsidiary companies as of the time of reporting.
- You don't work for Cybozu or its subsidiary companies as of the time of reporting under a contract such as a work delegation agreement, secondment agreement, dispatching agreement or the like.
- You have not been employed as regular fulltime employees of Cybozu or its subsidiary companies in the past.
- You have not worked in the product development and cloud service operation related work at Cybozu or its subsidiary companies in the past.
- You can communicate with Cy-PSIRT in Japanese or English.
- You agree with the Terms and Conditions for Cybozu Bug Bounty Program.

You can see the Terms and Conditions for Cybozu Bug Bounty Program at the following URL:
https://cybozu.co.jp/products/bug-bounty/en/pdf/terms.pdf
 
# 3.	Communication
## 3.1	Contact Us

This program is managed by Cy-PSIRT under Cybozu, Inc.  
Through the reporting site, you can contact us with your question about reporting vulnerabilities under this program. If you do not have an account of the reporting site, please apply it from the Reporting Site Account Request Form.  
Reporting Site:  
https://cy-bugbounty.cybozu.com/k/  
Reporting Site Account Request Form:  
https://form.kintoneapp.com/public/form/show/d16726f3de2ce25f846c43603fe7260c80a5adbc1ed878a7fcd66f8b671be525  


As for other questions, you can also contact us at our e-mail address.  
Email:  
productsecurity@cybozu.co.jp  

## 3.2	PGP Key
When reporters contact Cy-PSIRT, they can use a PGP key. The public key information is available at the following:  
https://www.cybozu.com/jp/features/management/cy-psirt.asc

# 4. Cybozu Vulnerability Information Handling Policy

All vulnerability information that is reported to Cybozu will be received and handled in accordance with Cybozu's "Vulnerability Information Handling Policy". The Vulnerability Information Handling Policy defines how we will handle and publicize any vulnerabilities that are discovered in the products and services that Cybozu offers. For details, see the following Japanese Web site:  
https://cybozu.co.jp/company/security-policy/
 
# 5. Response Process for Vulnerability Information
## 5.1 Response Process

A vulnerability reported from a reporter to Cy-PSIRT is evaluated by using the following process:
1.	We assign a "response number" and communicate it to the reporter.
2.	We examine the report to identify a vulnerability and calculate the reward amount.
3.	We contact the reporter with the evaluation results.
- The term "identify" means that we recognize a behavior in the services subject to the Program as a vulnerability. The recognition date of a vulnerability refers to the date when we identified the vulnerability.
- Once we decide whether or not to identify the reported information as a vulnerability, we will notify the reporter of the results.
- If the necessary information is not provided to identify the reported information as a vulnerability, we may contact the reporter to provide the additional information.
- At this point, the evaluation and the payment amount may vary.
4.	The reporter contacts Cy-PSIRT with "response completed", and then the response process is completed.
- When Cy-PSIRT notifies a result of the investigation, we mention the reply due date. Even if we do not receive a reply from the reporter by the due date, the response process is also treated as completed.
- At this point, the payment amount becomes fixed and will not be changed afterwards.


## 5.2	Order in Which Inquiries to Be Accepted
As for received inquiries, we accept them in the order of receipt.

## 5.3	Time for Acceptance
We receive vulnerability reports and inquiries from 10:00 a.m. to 5:00 p.m. (JST) on weekdays.  
Generally, received reports and inquiries are accepted within two business days. 

## 5.4	Order in Which Vulnerabilities to Be Evaluated
Generally, vulnerabilities are evaluated in the order of the response number. However, the evaluation order may be changed due to the vulnerability report status and so on. 

# 6. Rewards
## 6.1 Formula for Calculating the Payment Amount
The amount of the reward is determined according to the following rules:

### Products and Services
|Item| Summary|Case|Calculation method|
|--|--|--|--|
|1|Is it an RCE?|Yes|1,000,000 yen (Flat rate). Formulas 4 to 5 are applied.|
|||No|Formulas 2 to 5 are applied.|
|2|Vulnerability type|SQL injection | 60,000 ~ 250,000 yen|
|||Injection(except for SQL injection)|20,000 ~ 100,000 yen|
|||Permissions, Privileges, and Access Controls|20,000 ~ 300,000 yen|
|||Improper Input Validation|20,000 ~ 250,000 yen|
|||XSS|40,000 ~ 65,000 yen|
|||Others|10,000 ~ 300,000 yen|
|3|	Coefficients by product	|kintone<br>kintone Mobile <br> cybozu.com administration <br> cybozu.com operational base|	x 5|
|||	Garoon|x 2 <br> * Optional products are not included.|
|||Others|x 1|
|4|Maximum amount | | 1,000,000 yen for one (1) vulnerability in each product|
|5	|Additional payments by payee|Reporter|x 1|
|||Contribution|x 2|

### Web Sites
| Item | Summary | Case | Calculation method|
|--|--|--|--|
|1| Is it an RCE? | Yes	|1,000,000 yen (Flat rate)|
||| No | 20,000 yen (Flat rate).|
| 2 | Additional payments by payee | Reporter | x 1|
||| Contribution | x 2 |

## 6.2 Supplementary Rules on Earing Rewards

| Item | Summary | Rules | 
|--|--|--|
| 1 | As a result of investigation, multiple qualifying vulnerabilities are recognized. |The reporter earns rewards for vulnerabilities that the reporter reported. The reporter cannot earn rewards for vulnerabilities that we detect in the same product or other products as a result of investing in the report|
| 2 | Identical or similar vulnerabilities are reported. | When we receive multiple reports of vulnerabilities with the identical or similar cause in the same product, the first reported vulnerability information is identified as a qualifying vulnerability. Only the reporter of the identified vulnerability earns a reward.|
| 3 | A known vulnerability is reported. | If a reported vulnerability is the vulnerability that we have already recognized, the reporter cannot earn a reward.|
| 4 | A vulnerability is reported for an environment that is not supported.	| If a reported vulnerability is reproduced in an environment that is not supported, the reporter cannot earn a reward. For information about supported environments, see the Web site of each product|
| 5 | As a result of investigation, the evaluation results are changed. | If the score of the already-identified vulnerability is changed as a result of the investigation, the reward amount will also be changed according to the changed score only on the condition that the response process is not completed. |


### 6.2.1 Examples of Identical Vulnerabilities with the Same Root Cause
- Both input from a parameter and input from a hash object expose vulnerabilities.
- Multiple Web sites hosted on the same server expose vulnerabilities caused by the configuration of the environment.
- Different programs in the same product use the identical logic, function, and so forth, and thus they expose vulnerabilities.

This rule does not apply if identical vulnerabilities with the same root cause are exposed in different products.

### 6.2.2	Examples of Similar Vulnerabilities
- Different programs in a product are similar in logic and thus they expose the same vulnerability.

This rule does not apply if similar vulnerabilities are exposed in different products.
 
## 6.3 Delivery of Rewards
If our response process for a vulnerability reported by a reporter is completed, we will transfer the reward in cash at the end of the month after next.
Reporters must send their bank details to Cy-PSIRT. Note that we cannot transfer money to corporate accounts.  
The payment may take a long time or fail to be completed (a) if we do not receive bank details or (b) even if we make a bank transfer according to the provided bank details but the reporter cannot receive the reward.  

## 6.4	Donating Rewards
Reporters can donate earned rewards to an OSS community selected by Cybozu, instead of claiming the reward. If a reporter chooses to donate their reward, Cybozu also will donate the same amount as their reward to the OSS community. However, you must accept each reward in its entirety or donate it. You cannot split the reward between yourself and a donation.

### 6.4.1 Donation Recipients Selected by Cybozu
- Apache Software Foundation
- Linux Foundation
- OWASP Local Chapter in Japan

If a reporter does not specify a recipient, we make the donation to the Apache Software Foundation.

### 6.4.2 Donation Details
Once we have been contacted by a reporter saying that they wish to donate, Cybozu makes the donation within two months to the organization of the reporter's choice. The donation is made in the name of "Cybozu, Inc." Once the donation has been made, Cybozu notifies the reporter of the completion. We cannot accept requests such as issuing documents intended to be used for tax breaks, and so on. It is confirmed that the recipients listed above cannot enable a reporter to receive a tax break when the reporter lives in Japan.  
Taxation systems differ from country to country. For any countries other than Japan, please check the system by yourself.
 
## 6.5	Taxation in Japan
If the reward amount earned by the reporter exceeds a certain amount, the reporter has a duty to submit a final income tax return on their own. For details on final income tax returns, on the National Tax Agency's Web site as found below, see "1-12 Who Must File a Final Return" and "3-2 #8 Occasional Income" (page 32).  
http://www.nta.go.jp/taxes/shiraberu/taxanswer/shotoku/1900.htm  
http://www.nta.go.jp/taxes/shiraberu/taxanswer/shotoku/1490.htm

We do not issue payment records, because reporters do not need to attach payment records to their final tax return forms.  
The reporter may not be qualified as a dependent for tax calculations, even if the reporter does not have other income. However, this does not influence the dependent status for health insurance calculations. For details on exemptions for dependents, on the National Tax Agency's Web site as found below, see "3-3 #13 Exemption for dependents" (page 45).  
https://www.nta.go.jp/taxes/shiraberu/taxanswer/shotoku/1180.htm  

Taxation systems differ from country to country. Please check the system by yourself.
 
# 7.	Points
## 7.1	Calculation of Points to Be Given
In addition to rewards, reporters can earn points depending on their reports.
- The following are points for your reference, and the actual number of points will be decided by us.
- You may earn the sum of each item.
- Additionally, if we recognize the report as the practical information, points are given depending on the situation.

| Item | Case | Details | Point |
|--|--|--|--|
| 1	 |Vulnerability of product/service (excluding RCE) | A vulnerability of product or service is reported. | 10 ~ 40|
||Vulnerability of Web site (excluding RCE) | A Web site vulnerability is reported. <br> * Formulas 2 to 3 are not applied.|10|
||RCE | An RCE vulnerability is reported.|40|
|2|Accuracy of reproduction methods | We determine the number of points based on reported information.|0 or 10|
|3 |Clear description of the impact | We determine the number of points based on reported information. | 0 or 10|
|4| Impact on cybozu.com operational base | The target product is the "cybozu.com operational base". | 10 |
|5 | Cybozu award | We comprehensively evaluate reports for their severity for Cybozu, urgency, impact, and others and then, once a year, decide which reports we give the award to. <br>* The points are given when the decision is made. | 20 |

 
## 7.2 Benefits to Be Given for the Points
A reporter can receive a benefit when the reporter satisfies one of the following conditions for their points:
- The reporter earned 100 points in total within a specified one-year period.
- The reporter earned 300 points in total within a specified one-year period.  
\* Benefits are provided on a first come, first served basis. Benefits may not be sent if a reporter satisfies the condition after the end of the program period.
- The reporter is in the top three in the point ranking at the end of a specified one-year period.  
\* A reporter eligible for the delivery of the benefit may be determined by provisional points.

A reporter can receive each benefit by satisfying its respective condition.

## 7.3 Others
- When we prepare the evaluation results, points are provisionally vested. At this stage, points may increase or decrease depending on the evaluation results. When our response process is completed, points become fixed.
- We do not change points after the completion of the response process under all circumstances.
- Total earned points are accumulated on a yearly basis. You cannot carry over your points to the next year.
- The points cannot be redeemed for cash or other goods. 

# 8. Acknowledgments
Names of reporters who find and report vulnerabilities based on this program will be listed on the "Special thanks to contributors who have enhanced our service quality" page in token of our gratitude. Please refer to the following page for the details on who can receive the acknowledgement and when contributors are listed.  
https://cybozu.co.jp/products/bug-bounty/specialthanks/

# 9. Amendment of Rulebook
Cybozu shall be entitled to amend this Rulebook without prior public notification.
When amending a key portion of this Rulebook, Cybozu shall provide the reporters with notice of the details thereof. 

# 10. Testing Environment
See the Bug Bounty Testing Environment Program page.  
https://cybozu.co.jp/products/bug-bounty/#TestingEnvironmentProgram
 
