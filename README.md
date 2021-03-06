# LendingHome Case Study
![Re-Imaging The Mortgage Process](https://www.investorgreg.net/storage/real-estate/lendinghome.png)

## Overview

LendingHome is one of the nation's largest Hard Money Lenders having funded over 23,000 projects totaling over $5 Billion in funds [source.]( https://www.lendinghome.com/m/getRate/exitsLast24) LendingHome was incorporated in 2013 with the goal of transforming the process of receiving funding for a Single Family Bridge or Landlord mortgage into a faster, more transparent, and customer focussed process. James Herbert and Matt Humphrey along with Bill Trenchard (named as a Founding Advisor) successfully launched Lendinghome raising over $200 million in venture funding by October 2013 and originated their first loan just 6 months later in April 2014. The idea for LendingHome stems from James’ and Matt’s personal experiences being both borrowers and investors in the residential property space. During James Herbert’s interview with Lend Academy, he tells a story of how the bank took 104 days to refinance his own property and how difficult it was to get loans funded for his portfolios. These experiences lead him to create a company focussed on creating a better experience for the customer, one 
> “that was simple, fast, reliable, online, lower origination cost [source]( https://www.lendacademy.com/wp-content/uploads/2015/08/Podcast-44-James-Herbert.pdf )” 

and would also provide investors access to high quality loans.

 ---
	
LendingHome separates itself from crowdfunding sites by the amount of available capital. Since its inception LendingHome has had several large institutional investors that enable them to confidently fund loans without wondering if individual investors will be interested or if they have enough available capital. In an interview with Lend Academy James cites they have over $9 Billion in combined capacity from their institutional investors. LendingHome also pulls in funds from accredited investors who can diversify their investment across several loans. Some of the early institutional investors include: Charles Moldow (Foundation Capital is a Lead Series A Investor), Micky Malka at Ribbit Ventures, Joe Chen at Renren, Cowboy Ventures,First Round Capital and Colony Capital [source.](https://www.lendacademy.com/wp-content/uploads/2015/08/Podcast-44-James-Herbert.pdf) 

## LendingHome’s Business Model:
![](https://pbs.twimg.com/media/EnTHxr5XcAE7SBT?format=jpg&name=small)

Lendinghome is focussed on solving the speed and transparency problems that many borrowers face when applying for mortgages . The loan products they offer are for Single Family (1-4 units) homes and are structured as Bridge or Landlord loans. LendingHome is a data driven customer focussed organization that really has two sets of customers. The first set of customers is the borrowers who benefit from their streamlined application process that simplifies the complex process of getting approved for a loan & lowers origination cost compared to traditional lenders. LendingHome’s other set of customers are their accredited investors who also enjoy a user friendly interface, automated investing options and the ability to diversify their real estate investment portfolio.

---  

LendingHome’s target audience are the borrowers who may not qualify or want a bank loan for a myriad of different reasons. This target audience that LendingHome seeks to attract is the same large audience that has been going to hard money lenders for the past decades. The market size for the hard money sector is approximately $10 Billion [source.](https://www.realtymogul.com/knowledge-center/article/p2p-marketplace-lending-and-institutional-investors#:~:text=Most%20industry%20followers%20estimate%20that,money%E2%80%9D%20market%20size%20of%20approx) In other words these are borrowers who want to Fix & Flip a property or they are looking to create rental income by renting their property out. Some of the reasons customers are coming to LendingHome (or looking for a Hard Money Lender in general)  is that do not qualify for a bank loan because of: credit, number of properties owned( if over 10 properties they are disqualified them from Fannie loans which most banks sell their loans too), time to close (traditional lenders such as banks are not known for moving quickly), or another reason that has made a traditional, more rigours bank loan unattractive.

---

The solution LendingHome offers is a fast, online, customer friendly, transparent loan process. With many of the Hard Money Lenders in the market today, loans go through lengthy processes that are often opaque and may be declined for reasons that are unclear to the borrower. For investors LendingHome is offering an easy to use real estate investment platform where accredited investors can diversify their investments across high quality Single Family properties.

---

LendingHome’s competitive advantage is their commitment to providing a customer experience second to none. They have an online application that lets borrowers know in three minutes if they qualify for any of their loan programs and what interest rate they can expect. Borrowers can customize their loan request and see how different changes affect the rates they will get. If they decide to apply for the loan, the rest of the application takes about 15 minutes and shows borrowers through an interactive dashboard what they are missing, next steps and specific updates about their loan. LendingHome’s key differentiators are their focus on customer experience and available capital. In regards to customer experience, they claim to be the simplest, fastest and most reliable service in comparison to competitors. The other competitive advantage they can claim is being backed by large multi-billion dollar institutional investors giving them the security of knowing they can fund any project they extend terms too.

---

### LendingHome’s Tech Stack

LendingHome has an extensive tech stack that is constantly evolving as they add integrations and improve their platform.

Below is a bird’s eye view of their Architecture found on StackShare: 

> “The product is split into four major applications:
>- Consumer: A end-user facing application handling both the loan application process for the borrower as well as various investment management services for the investor.
>- Operations (ops): An internal application designed for our in-house loan specialists to handle every step of the loan from application to underwriting to servicing to final payoff.
>- Money movements: An internal application which integrates with our bank partners and exposes a simple API for sending ACH and federal wires.
>- Salesforce Integration: We’re a two-sided marketplace, and we keep track of both borrower and investor relationships using Salesforce. [source.](https://stackshare.io/lendinghome/how-lendinghome-scaled-their-marketplace-to-$750m-in-real-estate-loans )”

---
LendingHome started off using Heroku to deploy and scale their application layer as well as the database & caching layers. They also use Amazon Web Services for hosting and have recently been considering switching off of Heroku and solely using AWS.

---

For their front end they started off with simple 
> “server-side HTML rendered through Ruby on rails using HAML and jQuery. [source.](https://stackshare.io/lendinghome/how-lendinghome-scaled-their-marketplace-to-$750m-in-real-estate-loans) ” 

This helped LendingHome get launched more quickly because of the simplicity. As their frontend became more advanced they transitioned into using multiple single page web apps built with React, Redux, ES6 and Webpack.

---
LendingHome’s development team has worked to simplify the backend by removing server-side rendering and creating simple endpoints instead. To service loans, (the process of making sure borrowers payments are made on time and that investors are paid back including interest) Lendinghome has built an end-to-end servicing engine that can read payment activity from subservices, collect payments from borrowers and pay investors the money they are owed. 

---

LendingHome uses PostgreSQL as its primary database. To communicate with their borrowers they use Twilio for SMS and voice and Mailgun for email. On the backend they also have an Automated Investing system that enables investors to automatically buy parts of loans as soon as they come available. Retail investors can also choose their own specific fractional notes but their choices are limited to three different types of investment programs. Their automated system, AutoInvest, handles this process. 

---

LendingHome has also built an extensive document generation and parsing framework to handle the mortgage contracts that typically have over 1,000 pages. The main components are DocGen, CloudConvert, RightSignature and wkhtmltopdf. Their process to handle documentation, particularly DocViewer, automatically parses data and speeds up loan processing time reducing the workload of LendingHome’s staff. 

---

LendingHome is committed to continuous integration and testing stating that their 

> “ test suite consists of over 30,000 tests that run hundreds of times a day...We use RSpec for core testing, and Capybara/Poltergeist for headless integration tests [source.](https://stackshare.io/lendinghome/how-lendinghome-scaled-their-marketplace-to-$750m-in-real-estate-loans )”

 When they first launched they were using CircleCI but have recently transitioned to BuildKite because it gives greater granularity into figuring out where tests have failed.

---
Another major part of LendingHome’s platform is that it was built to be able to handle lots of third party vendor integrations. They currently have over 50 vendor integrations that perform tasks such as pulling property data, finding home price trends, checking borrower creditworthiness and investor credentials. One of the vendors they use is BlockScore which checks the OFAC (Office of Foreign Assets Control) to make sure a borrower or investor is not on a prohibited list. This integration adds to the proficiency of LendingHome’s app and reduces workload on internal staff.  Another useful integration comes from Lob which verifies mailing addresses and notifies users when there are errors. LendingHome also uses InvestReady to verify their investors accreditation since at this time all of their investors must be accredited. 
> “Other noteworthy integrations include RedBell, LPS, ClearCapital, Zillow, Walkscore, Trulia, RentRange, and CredCo [source.](https://stackshare.io/lendinghome/how-lendinghome-scaled-their-marketplace-to-$750m-in-real-estate-loans )”

---

The mortgage industry relies heavily on data to determine the risk of a loan, taking into account many factors that include data about the borrower, the property and surrounding properties. LendingHome, styling itself a Data Driven Organization uses Amazon Redshift and their Postgres database to model credit default probabilities and stress test various scenarios to mitigate risk. They also use Looker as the front end to the Amazon Redshift cluster. This addition helps them query databases, create complex dashboards and perform risk / credit modeling. Another major component to LendingHome being Data Driven is the tracking they do on their website, funnel analysis / user retention tracking and managing the efficiency of their many front end integrations. They use Google Analytics, Mixpanel and Segment respectively to capture & analyze the data. In regards to Source Code Management, they have been using GitHub since day one.

---

Performance and Monitoring is a top priority for LendingHome because they realize that latency or errors experienced by users can equate to thousands of dollars lost in potential origination costs. To stay on top of what is happening real time LendingHome uses several tools. They use Sentry for error reporting. FullSory is used for monitoring exactly what users are doing on any part of the application and can help reproduce any issues. Pingdom is their primary monitoring and uptime reporting tool which automatically sends SMS and Slack alerts. They also use New Relic which helps the team identify what is causing page timeouts and latency. 

---

Lendinghome is currently practicing an Agile methodology using Jira for issue tracking. In the beginning they just used a google doc knowing they were not ready to use all of the features JIRA offers. Slack and Google applications are the main methods for communication.

Salesforce & Marketo are used by their sales team to track clients, lead scoring and marketing. When LendingHome looks to build user-facing features they like to use Sketch and Invision to create mockups first. This allows for a streamlined design process where they are able to spend less time re-building features. 

---

LendingHome is committed to continually growing and constantly improving their platform so their tech stack is ever evolving. Visit this site to see the current tech stack:  [StackShare - LendingHome Tech Stack](https://stackshare.io/lendinghome/lendinghome) --- 

## The Landscape Surrounding LendingHome:
![](https://i.insider.com/5d2757d1a17d6c2d970283e3?width=1300&format=jpeg&auto=webp) 


LendingHome clearly identifies itself as a FinTech company looking to disrupt the Lending domain of the financial sector. LendingHome is focussed on providing mortgages of under $1 Million in Bridge and Landlord products for Single Family homes making them a clear competitor in the Mortgage Industry - A Multi-Trillion Dollar Industry! 

---

The Lending domain like many other areas of the financial sector has seen some major trend shifts over the past decade and is set to continue to see trend changes throughout the next decade. Below are a few of the major trends that I believe will have a major impact on the Lending Domain.

 ---

**Full Spectrum Credit Scoring Adoption** -Currently a borrower’s credit or FICO score is a major factor for whether they will be eligible for a loan and how expensive their loan will be. As the use of AI increases some lenders are starting to use Full Spectrum Credit Scoring which seeks to create a more complete picture of a borrower's ability to repay loans. This type of credit scoring takes into account many additional factors such as: payment of monthly bills, use of payday or subprime lending options, online borrowing, inventory turnover, overall profitability, and several other factors. Using data analytics and AI will enable lenders to get a more complete picture of the risk associated with the potential borrower, enable more borrowers to be eligible for a loan, give borrowers more fair loans, and reduce risk while increasing profit for lenders.

---

**Growing use of Artificial Intelligence** - In the same lane as the trend mentioned above many financial institutions including major lenders are investing heavily and utilizing machine learning to fully automate lending which reduces the time it takes to underwrite a loan & creates better risk assessment measures (such as the Full Spectrum Credit Scoring mentioned above). This creates an environment where loans can be granted much faster. The goal of incorporating AI into making loan decisions is to allow consumers to see fairer, better quality and faster loans.

--- 


**Open Banking** is a trend that has been changing the financial industry across the globe making data more accessible and curbing the competitive advantage of data rich companies, typically traditional financial institutions who are a major source for lending. 

---

**FinTech Leaders Are Attracting Billions** - FinTech Lenders are a major sector of the FinTech business boom and have played a major role in attracting Billions in investment dollars  from investors by offering borrowers a streamlined user experience that offers easier and faster ways to borrow money. Over the last 8 years investment in the Fintech sector has grown from 

> “$2 Billion in 2010 to over 50 Billion in 2018 [source.]( https://techcrunch.com/2019/12/22/fintechs-next-decade-will-look-radically-different/)”

---

**Improved Customer Centric Lending practices**  - Financial Services and Lending have traditionally not been known as sectors known for outstanding customer service or for putting a huge focus on user experience. As face to face customer relationships have declined coupled with the rise of online banking, traditional institutions have begun competing to make their platform the most customer friendly. As more customer experience focussed lenders enter the space it is forcing the industry to become more customer-centric or risk losing market share.

---

 
**Faster Business Loans** - For most of this decade a business waiting up to 6 months for a loan was something a business just had to factor in. As technology improves and more FinTech Lenders enter the space, businesses can expect much faster loans. 
> “In the next year, small business owners can expect more financial institutions offering approvals and funding in under 48 hours [source.](https://www.biz2credit.com/blog/2020/02/07/top-8-business-lending-trends-to-watch-in-2020-business-growth-loans/) ”

---

**BlockChain & Distributed Ledger Technology** -Blockchain technology is a disrupter that is changing the way many industries keep records and manage real time transactions. The Lending domain is no different. According to Biz2credit Blockchain technology is being developed to do the following:
- Leverage digital assets such as cryptocurrencies to attain loans
- Track and manage loan payments
- Provide real-time transaction data 
- Give borrowers more control over their loan
- Connect borrowers with private lenders
- Speed up the loan approval process
- Greater access to business growth loans [source](https://www.biz2credit.com/blog/2020/02/07/top-8-business-lending-trends-to-watch-in-2020-business-growth-loans/)”
---
 **Growth in Online Alternative Lenders** - Traditional large financial institutions and other major lenders have had strict requirements making it next to impossible for some borrowers to qualify for their loans. With the explosion of FinTech Lenders many of them have occupied the space of providing loans to less attractive borrowers and small business owners that would be denied by traditional lending institutions. While the interest rate offered by these lenders is typically higher, they offer loans to customers typically denied by banks, quick decisions, quick funding, low revenue requirements and merchant cash advances to name a few. 

---



### Major Companies In The Lending Domain
![](https://connectedinvestors.com/blog/wp-content/uploads/2015/08/The-truth-about-Hard-Money-Lenders-and-REI.gif) 

The Lending Domain of the Financial Sector is vast space with many competitors. Below I will focus on two more traditional leaders in the Mortgage space, QuickenLoans and Amerisave Mortgage Company. Below I will also look at the leading FinTech companies in the Lending domain: LendingClub, SoFi, and Prosper.

---

Here are two lists of competitors to LendingHome that could be used to compare business performance depending if you are looking at companies in the mortgage space or emerging Fintech companies in the lending domain.  

---

**Major Mortgage Companies**: 

---

AmeriSave Mortgage, Brex, Better Mortgage, Home Loan, William Ravies Real Estate, Mortgage & Insurance, iCAP Realty Advisors, Eagle Home Mortgage, Eastern Union, Dacotah Bank, Quicken Loans.

----


**Fintech Competitors in Lending Domain**:

---

Blend, Avant, Qudian, SoFi, Affirm, Borro, Funding Circle, GoRefi, Kabbage, LendingClub, OnDeck, Orchard, Prosper($5 Billion loans originated - claiming third after LendingCLub($16 Billion) and SoFi($6 Billion), ZestFinance, Salt Lending, Tala, OppLoans, Bond Street, Braviant Holdings, Fundbox.

---



## The Bottom Line - How LendingHome compares to Leaders of the Lending Domain

LendingHome is without a doubt a force to be reckoned with in the Hard Money Space. From day one they recognized a vulnerability in the Hard Money Sector, 
> “extreme lender fragmentation, a terrible borrower experience (uncertain terms, hidden fees), and an imbalanced risk-reward profile, [source.](https://www.businesswire.com/news/home/20180405005425/en/LendingHome-Wins-HousingWire-Tech100-Award-for-Second-Year) ” 

and set out to take advantage by building their platform from scratch designed to offer a fast, transparent online experience while also keeping the quality of their loans high enabling them to position themselves as a marketplace lender with institutional investor backing. Since launching, LendingHome has won several awards including two second place spots on the HousingWire Tech100 list. Their founders dream of creating a product designed to exploit the vulnerabilities common to most hard money lenders in the industry has become a reality! LendingHome has overcome development obstacles and has now funded over $5 Billion across 23,000 projects, according to their website, making it clear their business model works. LendingHome’s achievements will definitely force other Hard Money Lenders to re-evaluate their own process if their market share continues to grow as it has been.

 ---


### Core Metrics - The Numbers Don’t Lie:

The main metric lenders use is the total dollar amount of loans they have originated. Leading this metric in the fintech space is LendingClub, SoFi and Prosper. LendingHome boasts an impressive $5 Billion plus  loans originated since launch but unfortunately these statistics are not uniformly disclosed  publicly. To compare these companies lets look the metrics Revenue reported in 2019, # of full time employees, Date Founded and the ratio of Revenue to # of full time employees expressed as Revenue produced per Employee =  Revenue / # of employees. 

---
 
The statistics expressed in the table below are statistics for 2019 found on ZoomInfo.com:
![LendingHome V. Leading Lenders](https://scontent.fatl1-2.fna.fbcdn.net/v/t1.0-9/128096889_199381811792054_6329962835951969985_n.jpg?_nc_cat=106&ccb=2&_nc_sid=730e14&_nc_ohc=c3sUFKUnfcYAX_mUu_y&_nc_ht=scontent.fatl1-2.fna&oh=9b75a93bd8ae948e6205547fac635feb&oe=5FEB5AF2)

 ---

The Lending domain, more specifically the Mortgage space is a multi trillion dollar industry dominated by many traditional institutions some of them reporting multi billions in revenue in 2019. Companies like LendingHome have come into the space as disruptors looking to create a customer focussed loan process that is faster, more transparent & still produces high quality investment options for investors. LendingHome along with several other FinTech lenders have successfully broken into the space and are forcing larger traditional institutions to recognize them as competitors.

 ---

LendingHome reported $65 Million in revenue with 300 employees in 2019 according to ZoomInfo. Since LendingHome was founded in 2013 it has had less time to capture market share than large mortgage lenders like QuickenLoans or even other Fintech companies like LendingClub. To compare these companies revenues lets focus on Revenue / # Employees to see how much revenue is produced for each full time employee on average. At $218,000 per employee LendingHome is below both FinTech leaders in the lending space SoFi ($513,5333) and LendingClub ($493,237). LendingHome is also well below more traditional mortgage companies like Quicken Loans($517,647) and AmeriSave Mortgage Company($333,016). These comparisons show that LendingHome is clearly not a leader in the mortgage lending space at this time. This being said, with LendingHome claiming it has already originated over $5 Billion in loans in just over 5 years, LendingHome is showing they are here to stay and will continue to take market share. There are many competitors in the lending space and many of them are focussed on servicing borrowers that have not had the best experience with the more traditional banks. With a focus on improving the customer experience by making the loan process quicker and more transparent, LendingHome is in a good position to attract more borrowers looking for Single Family Bridge and Landlord loans. The question remains to be answered if their customer experience focus is good enough to continue to pull market share away from larger traditional lending institutions and hold market share from other emerging Fintech lenders with a similar focus on customer experience and an expedited loan process.

---  


## Recommendations

My advice to LendingHome would be to expand the loan products they offer  - right now offering only Single Family Bridge and Landlord loans with a max loan amount of $1,000,000 is limiting the amount of money they can make from origination fees (typically 2.5% of the loan). I would begin offering multifamily bridge products for loan amounts up to $10 Million. I would definitely make the requirements for the higher loan amounts more stringent so that there can be no argument that these loans are high quality.

---

This recommendation comes from looking at the leading Fintech companies in the Lending Domain. Both SoFi and LendingClub offer multiple loan products while LendingHome currently offers two - the Single Family Bridge loan and Single Family Landlord loan. While I think it is important for LendingHome to stay within its defined niche -real estate(1-4 units currently)- I think it will be highly profitable if LendingHome expands their business model to include other types of real estate. As many in the real estate industry know, multifamily properties often require much higher loan amounts which would exponentially increase the origination fees charged and collected, increasing LendingHome’s revenue. While I understand that multifamily property deals are more difficult to underwrite and originate than single family property deals. I also must point out that the success they have experienced with their platform should be a sign that it can be done and will really only be a next step of what LendingHome has already accomplished with their platform. LendingHome would not need to bring on any additional technologies to accomplish this goal. They can continue to use the same tech stack but add a similar process for multifamily loans and loans over $1,000,000. For these loans I would suggest factoring in the borrowers experience with properties of similar size and raise the minimum credit worthiness standard.

 ---


In conclusion, LendingHome is a market disruptor in the financial sector, lending domain and most specifically the Hard Money space. The success their platform has seen is a sign that a customer focussed, fast and transparent process can work for both investors and borrowers. I look forward to watching their continued growth and how the market adapts to their success.

--- 









**Additional sources**: 

---

[1](https://stackshare.io/lendinghome/how-lendinghome-scaled-their-marketplace-to-$750m-in-real-estate-loans) 

[2](https://www.biz2credit.com/blog/2020/02/07/top-8-business-lending-trends-to-watch-in-2020-business-growth-loans/) 

[3](https://empirica-software.com/fintech-companies-lending/) 

[4](https://builtin.com/fintech/fintech-lending-applications) 

[5](https://www.businesswire.com/news/home/20180405005425/en/LendingHome-Wins-HousingWire-Tech100-Award-for-Second-Year) 

[6](https://www.businesswire.com/news/home/20191216005173/en/LendingHome-Surpasses-5-Billion-in-Loans-in-Five-Years) 

[7](https://www.forbes.com/sites/jeffkauflin/2019/02/04/the-10-biggest-fintech-companies-in-america-2019/#5e6a3bc932b9) 

[8](https://www.accenture.com/us-en/insight-future-fintech-banking) 

[9](https://www.forbes.com/fintech/#39ae67bc13f1) 

[10](https://www.businessinsider.com/online-mortgage-lending-report) 

