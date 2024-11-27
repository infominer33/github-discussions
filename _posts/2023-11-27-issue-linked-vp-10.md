---
title: "Clarify: node out of consensus"
date: 2023-11-27 09:07:15 +0000
author: Echsecutor
excerpt: >
  Additional requirements:  
  1. The scope/domain of the types of entities/subjects addressed/named by a particular method
  2. Estimated size of each scope/domain (number of individual entities)
  3. Estimate of the daily transaction volume of each scope/domain (as an indicator of market size/opportunity)  
  For example:  
  > MWH> What is an estimate of the number of business documents exchanged every day in the world?  
  ChatGPT> The number of business documents exchanged daily worldwide is enormous, reflecting the scale of global commerce and communication. While exact statistics are difficult to pinpoint, industry estimates and studies suggest:  
  1. Global Estimates:  
  The IDC (International Data Corporation) estimated in recent years that the world generates over 330 billion emails per day, many of which are business-related.  
  E-invoicing and electronic documents alone account for over billions of exchanges daily. For example, the Billentis Report estimates over 550 billion e-invoices and related business documents are exchanged annually, averaging around 1.5 billion daily.  
  2. Physical Documents:  
  Traditional paper-based business documents (contracts, reports, forms, etc.) add significantly to this number, particularly in industries still transitioning to digital formats.  
  3. Document Types:  
  Examples of business documents include invoices, purchase orders, contracts, shipping documents, tax forms, and internal reports.  
  Conclusion:  
  A reasonable estimate places the daily exchange of business documents (both digital and physical) in the billions, likely ranging from 3 to 5 billion daily, depending on the context and medium of exchange.  
  > MWH> How many people fly every day?  
  ChatGPT> On an average day, approximately 2.9 million airline passengers travel worldwide, with the United States alone accounting for about 45,000 flights serving domestic and international travelers. Globally, estimates suggest that the number of daily flights surpasses 100,000, carrying millions of people between various destinations.  
  > MWH> What is an estimate of the average number of car parts manufactured per day?  
  ChatGPT> The global automotive industry manufactures an immense number of car parts daily. Estimates suggest that over 30 million individual components are produced each day. This figure reflects the large variety of parts needed for vehicles, including engines, transmissions, batteries, electronics, and other structural and functional components.  
  Key manufacturing hubs, such as China, account for a significant share due to their dominant automotive market and supply chain capabilities, which also contribute to the high global output. Other major regions include Europe, the United States, and emerging markets like India.  
  This production volume is driven by both Original Equipment Manufacturer (OEM) demand for new vehicles and the aftermarket for vehicle repairs and upgrades.  
  > MWH> What is an estimate of the number of drivers licenses in the world?  
  ChatGPT> The number of driver's licenses worldwide is estimated to be around 1.8 to 2 billion. This estimate is based on the global population of approximately 8 billion and varying rates of car ownership and license issuance across regions. In developed countries, where car ownership is higher, a significant majority of adults hold a driver’s license. For example, in the U.S., over 87% of adults have a license. However, in developing nations, this proportion is typically much lower due to differences in economic status and urbanization.  
  > MWH> What is an estimate of the number of times per day that a people in the world have to present their driver's license for identification purposes?  
  ChatGPT> Estimating the number of times driver's licenses are presented daily for identification worldwide is challenging due to varying practices across regions and uses beyond driving. However, an educated approximation can be derived based on key scenarios where licenses are commonly required:  
  1. Traffic Stops and Checkpoints:  
  Globally, billions of licensed drivers encounter routine traffic stops or checkpoints annually. For instance, in the U.S. alone, about 50,000 vehicle stops occur daily, many requiring license presentation.  
  2. Vehicle Rentals, Banking, and Identification:  
  Driver's licenses are widely used as primary identification for services like car rentals, bank transactions, and even age verification. With billions of transactions daily in banking and retail, a fraction involves license presentation.  
  3. Public and Private Sector Usage:  
  Many countries mandate driver's licenses as valid IDs for administrative purposes. For example, countries like the U.S. and Canada heavily rely on them in daily operations.  
  Estimated Total:  
  Considering these contexts:  
  If even 5-10% of the 2 billion license holders globally present their licenses daily, the total ranges between 100 million to 200 million instances per day.  
  This estimate may vary by region, urbanization, and dependence on licenses for non-driving activities. If you want data on a specific country or context, let me know!  
  > MWH> How many valid passports are there in the world and how many times per day are they presented for identification purposes?  
  ChatGPT> As of 2023, there were approximately 160.7 million valid U.S. passports alone, and global estimates suggest over 800 million valid passports worldwide. This reflects an increase in international travel and the expansion of passport issuance globally.  
  Regarding daily presentations for identification, passports are commonly used at border crossings, airports, and official transactions requiring high-security ID verification. With over 2.3 million people crossing international borders daily, passports are presented multiple times during travel (e.g., at departure and arrival). Additionally, passports are sometimes used for banking, legal, or other high-security processes, ...  
  > MWH> How many different pizza toppings are there and how many servings of these toppings are consumed daily in the world?  
  ChatGPT> Number of Different Pizza Toppings  
  There are thousands of potential pizza toppings worldwide, ranging from classic options like pepperoni and mushrooms to more unusual regional choices such as:  
  Traditional Toppings: Pepperoni, sausage, mushrooms, onions, and peppers.  
  Regional Specialties:  
  Japan: Squid, eel, and mayonnaise.  
  Brazil: Green peas, corn, and bananas.  
  India: Paneer, curry chicken, and tandoori spices.  
  Global Gourmet: Truffle oil, caviar, and exotic cheeses like gorgonzola.  
  While a comprehensive count is difficult due to constant culinary innovations, estimates suggest at least 2,000–3,000 distinct toppings exist globally, considering all cultural and gourmet variations.  
  ---  
  Number of Topping Servings Consumed Daily  
  Pizza consumption patterns help estimate the servings of toppings consumed:  
  1. Pizza Consumption:  
  Daily global consumption: Approximately 13.7 million pizzas.  
  Servings per pizza: Each pizza typically serves 2–3 people.  
  This results in roughly 27–41 million pizza servings daily.  
  2. Topping Servings:  
  Most pizzas feature 3–4 toppings on average.  
  This leads to 81–164 million individual servings of toppings consumed daily, assuming a balanced distribution.  
  ---  
  Pizza's versatility and cultural integration ensure its enduring global popularity, with toppings evolving to reflect local tastes and trends.
categories: decentralized-identity
tags: linked-vp
comments_file: linked-vp-issue-10_comments
permalink: /linked-vp/10/
url: https://github.com/decentralized-identity/linked-vp/issues/10
last_modified_at: 2024-11-27 08:35:29 +0000
---


**URL:** https://github.com/decentralized-identity/linked-vp/issues/10

After running the debian based container in the ID Union Test Network for a few days, the node is now out of consensus ("3.0"). Maybe the Pypi package should be replaced by the deb package for indy node 1.12.4, also adressing the missing init script issue https://github.com/IDunion/indy-node-container/issues/3