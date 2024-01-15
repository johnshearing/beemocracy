# Beemocracy2.0
Decentralize Governance By Jury For Cardano Modeled After The Democracy Which Evolved In Honey Bee Society  

Code implementation is in the planning stages  

Problems addressed:
Privacy, Identity, Bootstrapping, Low voter turnout, Selling delegation and votes, DRep Corruption, Lack of domain expertise, Whale control, Network traffic, Volume of on-chain data, Simplicity of code implementation.

#### **Modeling Cardano Governance On Bee Democracy**  
   
  * Abstract
    * Over millions of years, through the process of evolution, nature has worked out the form of democracy which produces the most truth and best decisions for honey bee colonies.  
      * Overview - [Bee Democracy](https://youtu.be/NDnQ4pAjBUg?t=310)
      * Tom Seeley, Cornell - [Details of Bee Democracy](https://youtu.be/JnnjY823e-w?t=2309)
      * Tom Seeley, Cornell - [BReps vs DReps](https://youtu.be/1x8T_CHZemE?t=122)
      * Tom Seeley, Cornell - [The Five Habits of Highly Effective Hives](https://youtu.be/XgSbPkInTzs?t=1929)
    * Evolution converges on these same decision making structures in many complex adaptive systems including the human brain.  
      * Scientific American - [You Have A Hive Mind](https://www.scientificamerican.com/article/you-have-a-hive-mind/)
      * National Institute for Health - [Cross Inhibition in Collective Decision Making](https://pubmed.ncbi.nlm.nih.gov/22157081/)
      * Science - [Inhibition in Collective Decision-Making](https://www.science.org/doi/10.1126/science.1210361)
      * Nature - [Psychophysical Laws and the Superorganism](https://www.nature.com/articles/s41598-018-22616-y)
    * Given enough time, Cardano governance will likely evolve the same structure. We can help speed things along.
    * As seen in the videos, bees don't actually vote.
    * The collective decision making process found in honey bee colonies for new home selection is basically a race to consensus using the following steps:
      * About two thirds of all the bees swarm outside the hive
      * Scout bees leave the swarm to look for suitable sites for a new hive
      * Scout bees return to the colony to report the direction and quality of a new home site with the intention of getting other scouts to examine the site.
      * If a certain number of scouts find themselves at a new home site all at the same time (from 10 to 20 implying ≈ 150 had inspected the site) that will trigger a "quorum reaction" in the scouts which causes all of them to return back to the swarm and guide the bees to the new home site.
      * That many bees are returning to give reports on various new home sites creates a race to get new scout bees to look at the best sights in order to be the first to obtain a quorum reaction.
      * What causes bees to arrive at a quorum reaction at the most suitable new home site is:
        1. The scouts always report longer and more enthusiastically when reporting better quality sites, so more scouts will go to those sites and then return to give their own reports.
        2. No scouts will give a report without first visiting the site for themselves.
      * So honest reporting when gathering consensus using only accurate first hand information is what the structure of Beemocracy2.0 enforces.
      * [Please listen to Tom Seeley in this video](https://www.youtube.com/watch?v=1x8T_CHZemE&t=123s) which is queued up to the correct moment when he explains the difference between bee democracy and human democracy. In the video he says that no decision maker advocates for a site they have not seen for themselves whereas in human democracy the decision makers often cast votes based on affiliation without ever investigating the matter for themselves. This is the quality that Beemocracy2.0 abstracts from the collective decision making process that evolution has selected for in the honey bee colony.
    * **By abstracting nature's results we can arrive at the optimum democracy which produces the best possible decisions in the shortest amount of time**
    * A race to consensus by voting is not possible in Cardano democracy because too much network activity in a short amount of time will jam the system.
    * So deciding governance proposals at jury trials will be used to ensure that all proposals are decided based on accurate first hand information only and without breaking the network.
    * In July 2021, the Ada Lovelace Institute, working with the University of Edinburgh and the Bingham Centre for the Rule of Law, convened 50 members of the UK public in two online, week-long citizens’ juries to deliberate on and recommend good governance practice with respect to administration of health data during a pandemic. The result was definitely not the government narrative. Developed by the Jefferson Centre in the 1970s, citizens’ juries are a type of structured deliberation with members of the public, sometimes referred to as a ‘mini public’. During facilitated workshops, participants –‘the jurors’ – are given balanced information and expert presentations about a chosen issue, before deliberating on that issue and reaching a conclusion of some kind. The issue usually addresses an area of public policy, and the conclusions generated often take the form of recommendations for policymakers. That the Ada Lovelace Institute at the University of Edinburgh is experimenting with governance by jury is encouraging to me.
https://www.adalovelaceinstitute.org/report/trust-data-governance-pandemics/
  * #### Process Overview
    * Beemocracy2.0 responds to all governance proposals by inviting any ADA holder to scout the proposal and then write a solicitation (a report) recommending how jurors should vote.
    * Scouts register their solicitation on the Cardano blockchain with their hardware wallet.
      * This binds their report and recommended vote to their digital signature.
    * The scout may remain anonymous and be known only by their collection of solicitations all having the same digital signature associated with their hardware wallet.
      * In this way, scouts (any ADA holder) gain history, reputation, and standing in the community without revealing their identity.
    * All governance proposals go before a jury to be decided. So a scout's solicitations are information and recommendations used to help the juries decide.
      * This means every ADA holder gets a voice with respect to governance proposals.
    * The jury is composed of randomly selected elite scouts - those ADA holders who have submitted at least 10 solicitations within the past 365 days. These 10 digitally signed solicitations with locked voting recommendations are used by the prosecution and the defense to evaluate the character of the scouts during jury selection. Prosecution and defense will alternate selections from a random pool of eligible scouts based on previous solicitations and some standard questions asked by the judge. If a scout is selected to serve on the jury and has written a solicitation on the current matter with an associated voting recommendation, then the voting recommendation is not binding. The scout/juror is free to listen to all arguments and decide anew.
    * So the solicitations serve two functions:
      1.  The solicitations are used to help inform juries when proposals are decided.
          * Think - scout bees examining various sites for their new hive.
          * Think - scouts coming back to the hive with **first hand information** to use in making a decision.
      2.  The solicitations are used to create a large educated jury pool of elite scouts who are invested by their anonymous reputation earned in the solicitation process.
          * Think - a guaranteed quorum of active, interested, and invested decision makers with first hand information to work with.
  * #### CIP-1694 - Governance by Centralized Jury Pretending To Be A Representative Democracy
    * Typical representative democracy such as Cardano's CIP-1694 has delegated representatives (DReps).
      * Community members delegate the voting power of their ADA to the DReps and the DReps vote however they want with the delegated voting power.
      * The DRep structure has no means to enforce that DReps debate nor is there any means to ensure they make decisions based on information they have verified for themselves.
      * The results of representative democracy are always echo chambers, information bubbles, ignorance, hysteria, cronyism, and ultimately very bad decisions for the community.
      * It is well understood that representative democracy always converges on corruption.
      * This is why IOG will appoint a jury of well informed highly respected community members (The Constitutional Committee) which shall have final say on governance issues.
      * So despite all the pretence of a representative democracy, governance issues in the Cardano community are ultimately decided by a fixed jury.
      * This is because juries of informed citizens typically make good decisions.
      * But a fixed jury appointed by IOG is not decentralized, and decentralized governance was the whole point of CIP-1694.
      * Solution: If we accept that the Constitutional Committee is just a jury, then we can see a way to transition to decentralized juries selected by anonymous reputation linked to community service via digital signature.
      * Beemocracy2.0 is that solution
 * #### Beemocracy2.0 - Governance By Decentralized Jury
    * Beemocracy2.0 has scouts (any ADA holder). 
    * Scouts can investigate a governance proposal and provide a solicitation (a report with a voting recommendation) to a jury of randomly selected elite scouts.
    * Elite scouts are community members who have written at least 10 solicitations of their own within the past 365 days.
    * Elite scouts are eligible to serve on juries which decide governance proposals.
    * These jury trials ensure that all governance proposals are debated using information collected by any ADA holder that has taken the time to prepare a solicitation.
    * Unlike the DReps in Cardano's CIP-1694...
      * The Beemocracy2.0 structure enforces that governance proposals must earn support through honest debate by randomly selected juries using information gathered by the community. The result is good decisions.
      * Scouts only receive consideration for the proposal they are currently soliciting (for or against) - Then consideration ends after the jurors have decided.
        * This is key to a functioning democracy - Scouts in the bee's world have to earn support for each proposal.
        * In human democracy like Cardano's CIP-1694 the delegated representatives only earn their delegation once and then learn to exploit their power for personal gain during the rest of their careers.
      * #### Scouts compete for delegation with no reward except for the survival and prosperity of their hive which includes their own survival and prosperity
        * If paying scouts for their work produced more truth than simply working for their own survival and prosperity then evolution would have selected for that.
      * Bee democracy is structured like so because those structured differently were all selected out of existence.
      * Cardano Democracy cannot be modeled on Human Democracy without becoming a selfish monster that self-destructs over time just like all the others. But if IOG abstracts the structure and feedback mechanisms found in Bee Democracy and applies these to Cardano Democracy then we will have governance that does not learn to create the very problems it was built to solve in order to feed and grow. Evolution already did the research. All we need to do is look at what the bees are doing. We should model Cardano governance on Bee Democracy -  the one which nature has perfected over the course of millions of years  
  * #### **Abstracting bee democracy functions and applying these to Cardano governance**
    * The data structure of this governance system is much like any online forum that we are used to.  
    * The governance is hosted on an immutable online forum for:
      *  Submitting and reading governance proposals 
      *  Submitting and reading scout opinions and their voting recommendations
    *  Any ADA holder can be a scout.
    * Scouts solicit for jury votes on each and every proposal they wish to weigh in on using an online document (a solicitation) which explains their position and which also locks their recommended votes. 
    * The mechanism is an on-chain transaction with a signed voting recommendation and the hash of the solicitation text on an immutable webpage.
    * The URL for any webpage on the Interplanetary File System (IPFS) is the hash of the webpage text.
      * **So the on-chain transaction with the signed voting recommendation and hash of the solicitation text points to the solicitation text on the IPFS forum webpage.**  
    * The scouts's voting recommendation is appended to the solicitation text and signed using their hardware wallet when the transaction is sent to the blockchain.
    * The scout's voting recommendation can not be changed once the solicitation has been published (Blockchain transactions are immutable).
    * The scout's collection of digitally signed solicitations on governance proposals becomes a very important part of their reputation.
    * A scout's reputation is used to determine their character in jury selection and is also used to determine the types of governance proposals they can help decide.
      * The reputation system will be tiered based on the following criteria with the higher ranked scouts serving on juries which decide cases that hold greater importance for the community:
        * the amount of solicitations the scout has written for or against governance proposals within the last 365 days
        * the amount of solicitations the scout has written for or against governance proposals since the scout has been active
        * the range of subjects the scout writes about
        * the number of times an elite scout has served on a jury
        * the types of proposals the scout has helped decide
        * how many times the scout's solicitations are cited by other scouts and by scout jurors when they decide cases
        * the types of cases they write about. Are they specialists in a particular area such as stake pool parameters, smart contracts, finance, ethics...?
        * the types of services they provide for the community
          * stake pool operator
          * library pool operator - helps store solicitations and governance documentation using IPFS protocol in a decentralized manner. Discussed in detail later in this document
          * creates educational material
          * respected youtubers
          * researchers
          * activists
          * Work at IOG, Cardano Foundation, Emurgo, government, partner corporations, DAOs
        * how often they add to or challenge other scout solicitations
        * how well their work is judged by other scouts
        * How many words on average are in the solicitations
        * and so on
      * All ADA holders can serve as scouts, which is to write solicitations and recommend a vote for or against a governance proposal.
        * These solicitations may be considered by the jurors. So everyone gets a voice as they gain history, reputation, and rank.
      * Jurors can get a lot of information from the body of solicitations even before reading them individually.
        * Solicitations will be aggregated by various categories so that jurors can get a sense of how the community feels even before reading the individual solicitations.
        * Jurors can also see who has recommended for or against a proposal.
          * While scouts can choose to remain anonymous, they may also choose to reveal their identities.
            * So if a juror sees that a solicitation with recommended vote is registered by Charles Hoskinson then they might give the proposal extra attention.
          * But each solicitation is linked by a hardware wallet to a scout's anonymous reputation, history, rank, and all the other solicitations associated with a scout's wallet.
            * This means that jurors can find out a lot of relevant information about a solicitation's author without knowing the scout's identity.
            * This gives Cardano governance the benefits of KYC without the problems.
        * The scout associated with a digital signature might be an individual, a group of people, and organizations such as an exchange, or even an artificial intelligence.
          * Who or what is the actual identity behind a solicitation's signature is not as important as the information presented in the solicitation.
          * This is because if it is determined that the solicitation misrepresents the facts then this will negatively impact the reputation invested in the digital signature.
          * So no matter if the scout is an individual, an organization, or an AI, the incentive is to provide accurate information.
      * Elite scouts, those ADA holders who have written 10 or more solicitations within the past 365 days, may serve on juries.
        * Notice that as the scout stops writing, it is assumed that the scout has lost touch with the issues and may no longer serve on a jury until they start scouting again.
        * This is very much the same as in actual honey bee society.
      * Scouts earn rank to decide proposals of greater importance to the community.
        * As scouts meet more and more of the criteria listed above they get to handle more and more types of cases and more and more important issues as they prove they are up to the tasks and ready to serve.
        * Lower ranking scout juries may handle smaller requests for funding.
        * Higher ranking scouts may serve on juries that decide higher value funding requests, parameter changes, constitutional issues, and emergency situations as they gain greater rank.
        * All of the scout's rank and privileges are automatically tied to their history and reputation by the same digital signature they use to sign all their solicitations and jury decisions.
        * All governance actions are automated and triggered by multisig transactions that check the ranks of all the jurors.

      * Governance System Structure In More Detail
        * The original governance proposal is also the first solicitation for the proposal.
          * The hash of the solicitation text and the scout's voting recommendation in support of their proposal goes on chain in a signed transaction.
          * The hash of the solicitation text is also the URL of the document when posted using the IPFS protocol.
          * So the proposal/solicitation transaction on the Cardano blockchain is linked to the text of the proposal (1st solicitation) on the IPFS webpage via the hash of the solicitation text.
        * Other scouts will wish to comment on the proposal and make a voting recommendation.
          * Scouts will write solicitations of their own which get linked to the original proposal.
          * The solicitation transaction is assembled as follows:
            * The voting rcommendation (For | Against) is included in the transaction.
            * The text of these solicitations are hashed and included in the transaction.
              * Again, this hash is also the URL of the webpage that holds the solicitation text.
            * The solicitations (For | Against) also have another field in the on chain transaction which is just the hash/URL of the original proposal.
              * This establishes the new solicitations as children of the original proposal.
              * So it is easy to make a webpage that links the original proposal/solicitation with all the children solicitations underneath.
        * Linking Comments Where Scouts Can Show They Changed Their Mind Even If They Can't Change Their Vote.
          * These would be a signed on chain transaction with the hash of the retraction text, or hash of additional comment.
            * This serves as the IPFS URL and makes it impossible to tamper with the text. 
            * Another field in the transaction is the hash of the scout's solicitation for which they now wish to comment on.                  
            * This establishes exactly what previous solicitation they are commenting on.
            * This makes the retraction a child of the scout's solicitation and the solicitation is a child of the original proposal.
            * So now the retraction gets listed under their original solicitation and jurors can see that the scout now regrets the vote.
            * DReps in CIP-1694 are elected rulers.
            * Scouts collect and share information so that the juries can make good collective decisions.
        * Trials for governance proposals end when each juror casts their vote and explains their decision with a solicitation signed with their digital signature. Then jurors sign a multi-sig transaction which binds all their decisions to end the trial. Smart contracts check the ranks of all the jurors to verify they have the permissions to decide the proposal and then the smart contracts automatically distribute funds, change parameters, or take some other governance action. The forum webpage will show how the jury decided.
        * Prevent Spamming The Blockchain With Solicitations
          * Perhaps smart contract validation could ensure each scout can publish only one child solicitation to comment on a governance proposal.
          * An alternative method of enforcement is reducing rank associated with a digital signature for spamming the blockchain with solicitations.
          * A fee might also be charged for posting solicitations to reduce spamming and to cover the cost of maintaining that record.
      * #### We will need filtering tools in our blockchain explorers to help forum operators organize the volume of solicitations. 
      * #### Staking To Pay Library Pool Operators For Hosting IPFS Immutable Webpages Which Host the Online Forum For Governance Proposals, Solicitations, Debate, Jury Decisions 
        * We will need an immutable website using the decentralized IPFS protocol which presents a forum to contain the text and the hash for all governance proposals and all scout solicitations, for or against the proposals. 
        * Everything on the governance website must persist for all eternity so future generations will know why we made the decisions we made.
        * With every governance proposal and solicitation, there must be a payment in ADA to cover the cost of hosting the proposal and to prevent spamming the system.
        * Library Pool Operators
          * This ADA will be staked in a random stake pool, and automatically, the staking rewards will be distributed to the owners of the computers which host the proposal webpages on the IPFS by lottery as follows.
          * Distributing the staking rewards by lottery allows market forces to promote redundant copies of all proposal webpages.
          * The rarest documentation will receive more rewards than documentation which is highly redundant throughout the system to incentivize even distribution.
          * There might be a small fee for serving each document paid by the consumer to prevent DOS attacks and to pay for bandwidth.
          * At random intervals, one of the hosted webpages (selected by lottery) for a given proposal will be requested and hashed to ensure the data is accessible and that the contents has not been altered.
          * The IPFS address and the document hash should be the same if the document has not been changed.
          * If the proposal webpage is returned unaltered then the host is paid the staking rewards associated with that lottery slot.
          * If the proposal webpage is not returned by the host computer then the host does not get paid the lottery reward, and the lottery is repeated with another host for that proposal webpage selected at random.
          * If a host fails again to return the data the next time it wins the lottery then it is removed from the index of hosts for that governance proposal.
          * So document hosts get paid by lottery in much the same way as Cardano stake pool operators get paid.
        * In this way the proposal webpage and all associated solicitations will persist for all eternity in a decentralized manner.
        * It may be that the cost of bandwidth and hashing power are too expensive to allow verification for proof of bandwidth and proof of storage. It is my understanding that currently the consumer/tester must request the entire document, and the host must provide it in a timely manner. Then the consumer/tester must hash the document to ensure that it matches the IPFS address of the document. This may be prohibitively expensive and is perhaps one reason that decentralized document storage has not caught on despite all the money which has been spent developing the idea. One compromise which proves the host at least has the document is to send the host a random number that is to be appended to the document. The host then hashes the document and sends back the hash to the consumer/tester. This requires much less bandwidth. Then the consumer/tester hashes the document along with the same appended random number. If the hash is the same then the consumer/tester knows that the host at least is in possession of the document. The problem with this approach is that the consumer/tester must also have the document in order to hash it. Of course the consumer/tester will not have copies of the governance documents so another solution is needed. I am no expert, in fact I am not even a novice, but it seems to me that recursive zero knowledge proofs, which will likely be available with the Midnight sidechain, solve this problem. If my understanding is correct, by using ZKPs it may be possible to prove that the document host has the document defined by its hash without the verifier needing to see the actual document. So Cardano could be the first to market with an inexpensive way to prove a host is at least in possession of a document. Then the consumer/verifier could request just a small part of the document chosen at random to ensure that documents are delivered in a timely manner. Reports from general consumers could also be used to verify bandwidth and document availability of governance documents.
      * Constitutional Committee Votes, Elite Scout solicitation voting recommendations, jury votes, and Stake Pool Operator votes to remain transparent by virtue of the solicitation process which also asks all to explain their votes and leave a body of information so that future generations will understand why those decisions were made.
      * **The Bee Democracy Structure Ensures That:**  
        * Scouts are incentivized by investment in their own reputations to provide accurate information in their solicitations and voting recommendations.
        * Jurors have lots of good information from solicitations to make their decisions 
        * Jurors are incentivized by investment in their own reputations to make good decisions for the community
        * Uninformed and uninvolved ADA holders don't serve on juries  
        * Reputation, history, rank, and collection of previous solicitations help in jury selection from a randomized pool of potential jurors.
        * Jurors must explain their reasoning on every vote for or against a proposal.
        * A body of literature remains (the solicitations) so future generations will understand how we came to our decisions and what they should consider before making changes
        * Scouts can remain anonymous, building reputations only on their body of solicitations and public service which all have the same digital signature. No KYC required.
       
#### Possible Exploits
  * Loading the Random Jury Pool With Elite Scouts Under The Control Of A Special Interest
    * The investment in becoming an elite scout and earning rank and privilege must be so high that the cost of generating several disposable elite scout identities sufficient to load a jury with digital signatures controlled by a special interest will be prohibitively expensive.

#### **Constitutional Amendments: Protecting Cardano From Becoming Like The Central Banks Or From Being Enslaved By Them**
  * [Right in the Bitcoin genesis block is a reference to a newspaper article about the abuse of central banks.](https://en.bitcoin.it/wiki/Genesis_block)  
So right from the beginning we know the purpose of blockchain is to offer humanity a decentralized alternative to central bank tyranny.  
Now we need to ask, what is it the central banks do which is so harmful?  
The central banks take commodities and turn them into receipt money, then fractional money, and finally into fiat money.  
Then they print as much money as they want which is the exact same thing as stealing because it devalues the citzen's money in the exact same amount as they print.   
Then they use this money to destabilize the world because speculation is most gainful during times of hardship and fear.  
[The article "All Wars Are Banker's Wars" is linked here.](https://whatreallyhappened.com/WRHARTICLES/allwarsarebankerwars)   
[The video presentation of the same article is linked here.](https://youtu.be/BrKf9nYeXT0?si=uD4I5R0J1mMQ_XQi)   

  * With BlackRocks new Bitcoin ETF we are now seeing the conversion of Bitcoin from commodity to fiat.  
This video queued up at the relevant time shows one scenario of which the central banks have many.  
https://youtu.be/eIVKezt-syo?si=67ne2Cg-Mo4PdNKi&t=609  
You can see in the video that BlackRock maintains the option to choose which fork of Bitcoin they will honor.   
Basically, BlackRock maintains custody of customers Bitcoin - Now Bitcoin is receipt money not a commodity.  
Now BlackRock can take in more Bitcoin investment than it holds and lend it out - Now Bitcoin is fractional money.  
Finally, BlackRock starts a panic by making investors aware that there is not enough Bitcoin to cover all investors.  
Blackrock saves the day by forking Bitcoin with some changes that allow Blackrock to print more Bitcoin. - Now Bitcoin is Fiat money.  
Extra surprise! Bitcoin is now a CBCD.  
  * Decentralization Alone Can't Stop Cardano Governance From Becoming Like The Central Banks Or From Being Enslaved By Them.
    * **Constitutional Amendments Required:**
      * **The Free Market Will Determine The Price Of ADA**
        * The price of ADA will not be set in relation to any other commodity nor any other currency by any authority. 
      * **No Oracles Will Be Used To Decide Any Governance Issues** 
        * Community members are responsible for determining what is true and expressing it with solicitations, debate, votes, and delegation
        * The free market will determine prices - not oracles
      * #### Constitutional Committee members will be compensated with ADA and will agree to hold only ADA in their portfolio and no other assets of any kind.
        * This helps ensure that the incentives of the Constitutional Committee are in alignment with their responsibility of adding utility and value to the protocol.
      * #### **ADA To Be The Only Form Of Currency Accepted Into The Treasury**
        * No receipt money shall be accepted into the treasury: 
          * Receipt money means you get a receipt for a commodity being held somewhere presumed to be safe
          * History shows that all banks will eventually succumb to the temptation of lending out the commodity backing the receipt, either in secret or publicly as fractional reserve banking.
          * This started in the middle ages when goldsmiths would hold gold in their safe for customers and provide a receipt which could be redeemed for the gold. Eventually the receipt became accepted as payment for commodities. But the goldsmiths would always lend out the gold to gain interest without telling the owners and would eventually default when the community discovered, leaving the customers with nothing. The most recent example of commodity-backed money was the US dollar which up until 1933 could be redeemed for gold at at $20.67 per troy ounce. Then it transitioned to fractional money when the price was changed to $35 per ounce in 1934, effectively reducing the value of the dollar by almost 41%. Then it transitioned to fiat money in 1971 - not redeemable for anything, but which citizens are required by law to accept. This is not the exception, this is the absolute rule. All commodity-backed money is a commodity in transition to fiat money. My understanding is that history has no exceptions to this rule. This information comes from [The Creature From Jekyll Island.pdf](https://drive.google.com/file/d/1Aj4rGWnTLvmXzG_gP0Xw_mM7T4Rnb3zi/view?usp=sharing). The transition may take several years but history shows that commodity-backed money always transitions to fiat money eventually. This has been going on since the middle ages and we now stand in a place where we can stop it.
        * No Stable Coins shall be accepted into the treasury
          * Stablecoins are just commodity or fiat backed overcollateralized receipt money in a new slick package. We have all seen what happens to stablecoins. Worse, all stablecoins that I know of are centralized money and require an oracle to function. So if spending requires using a stablecoin then the exchange must occur at the point of sale. Forbidding centralized currency forbids stablecoins and receipt money and commodity-backed and overcollateralized money. But we should forbid these explicitly. One thing we can not do is accept commodity-backed and overcollateralized money and stablecoins and then forbid centralized money because this is a contradiction - these are all centralized money.
        * #### No Algorithmic Stable Coins shall be accepted into the treasury
          * With Djed for example, we hear from Shahaf Bar-Geffen who is the COTI CEO that [Djed may be collateralized with a basket of different coins not just ADA](https://youtu.be/PipEUycQwfA?t=978). Another coin called Shen is already used in the process. I can't find much out about Shen - I don't know if it is a blockchain or a DAG like COTI. Further more, Djed is pegged to the dollar. So if you put $20 ADA in to the contract then you get $20 of Djed minus a fee for the exchange. When you want to cash out then you give your Djed back and get your $20 dollars worth of ADA back minus fees again. But what about inflation? Your $20 minus the fees is worth less because of inflation. So you suffer a loss because the dollar will be worth less when you go to get your ADA back. And if the dollar tanks then you are really in bad shape. Another concern is that Coti was associated with Ardana, and we all know how that went. Seems like the only reason to hold Djed in the Cardano treasury is if you think the price of ADA is going to fall. Does Cardano want to bet against itself? Reminds me of The Big Short. With all these questions about Djed and with all the bad history we have with stable coins it seems we should explicitly forbid holding them in the treasury.
        * Nothing that has physical existence such as buildings, land, equipment, timber, or gold shall be accepted into the treasury 
          * Physical things can be confiscated or associated with a country or a government. 
          * Right now in the news we are seeing that Binance is surviving Choke Point 2 because Binance has no physical offices.
        * No Central Bank Digital Currencies shall be accepted into the treasury as these can be disappeared by the issuing authority. 
        * No digital commodities other than ADA will be accepted into the treasury
          * Receipt money, commodity-backed money, overcollateralized money, fiat money, fractional money, stable coins, algorithmic stable coins and CBDCs. That leaves only digital commodities like Bitcoin and ADA. But holding Bitcoin is betting that it will surpass ADA in value. It's betting against our own project. 
        * No digital commodities from within the Cardano ecosystem other than ADA will be accepted into the treasury - No other tokens and no NFTs
          * So the only money left standing is ADA, NFTs and perhaps Midnight when that arrives.
ADA is preferable to Midnight because ADA is completely transparent which is very good for governance.
          * History has shown that when a treasury holds more than one commodity (gold and silver) in the treasury it was difficult to establish a fixed price ratio between the two metals. This problem is known as the bimetallic standard problem. The problem arose because the relative values of gold and silver fluctuated over time, depending on supply and demand factors. The problem with the bimetallic standard was eventually resolved with the adoption of the gold standard, which established gold as the sole standard for currency. This made it easier to maintain a stable value for the currency and reduced the risk of currency fluctuations. We should remember this lesson from history and only accept ADA into the treasury - not NFTs nor anything else except ADA.
        * There are times when Cardano governance will need to handle currencies other than ADA. For instance, we are required by law to accept fiat money like US dollars. But all currencies must be converted to ADA immediately upon receipt before going into the treasury. If spending requires using anything other than ADA then the exchange must occur at the point of sale. The whole point of ADA is to end slavery to the central banks. We must not give the banks a backdoor into our economy. We must not allow any form of money into the Cardano treasury except ADA. 
        * Why so explicit on only allowing ADA into the treasury:
If we are not explicit that only ADA is to be accepted into the treasury and if we don't explain why then future generations who have forgotten the horrors caused by other forms of money will allow them into the Cardano treasury.
      * **Treasury Will Never Engage In Borrowing Or Lending Of Any Kind**
        * No lending using promissory notes. This should be impossible if payments and donations are only made in ADA but should be explicitly stated so there is never a temptation to lend with promissory notes. Same as saying no double spending but banks make their money by double spending (Fractional Reserve Banking).
        * The treasury shall only receive ADA from protocol services such as staking fees and transactions fees. It will never borrow.
        * The treasury will only disperse ADA to make donations or to purchase services for the community in transactions which are ratified in governance elections.
        * Why Prohibit Cardano Governance From Borrowing and Lending:
Big Bank engages in predatory lending at the nation state level.
This is how they enslave poor countries and poor people.
Lets protect the Cardano nation from both becoming the prey or becoming the predator:
        * Why so explicit about never engaging in borrowing and lending?
          * The power to print fiat money was never explicitly granted to the federal government in the Constitution. In fact the authors voted against granting that power. Sadly they never specifically prohibited fiat money. So the power to print fiat money was reserved for the states or the people by the Tenth amendment. But of course the federal government does it anyway. The back door was Article I, Section 8, Clause 2 which reads as follows: *"The Congress shall have Power To... borrow Money on the credit of the United States."* Because you have to issue a note to acknowledge the debt, this opened the door for fiat money. The courts have upheld this interpretation. 
          * So it is not enough to not grant a power - some powers must be explicitly revoked.
      * **Explicitly recognize in the constitution that governments are complex adaptive systems that will learn to create the very problems they were instantiated to solve if money or benefits dispersed are allowed to feedback into the government agencies from which these originate.**
        * This is discussed in detail on our own Cardano governance forum [at this link here](https://forum.cardano.org/t/cardano-constitution-could-be-the-first-in-human-history-to-manage-government-as-a-complex-adaptive-system-an-intelligent-living-thing/116058?u=johnshearing).
The software to run Cardano governance is a **complex system**. But the Cardano governance as it helps the community manage itself is a **Complex Adaptive System**. Complex Adaptive Systems are living, learning, feeding, growing, evolving things. The United States Bank/Government is a Complex Adaptive system which learned to create the very problems it was built to solve in order to feed and grow. This is why we have never ending financial crises and never ending war. Voltaire now makes the Cardano Complex Adaptive System a Bank/Government too. It is a new living thing. It doesn't have to grow up learning to create the very problems it was built to solve like the US Bank/Government did.
Bee colonies store honey and make decisions in democratic elections. They are simple Bank/Governments and they are Complex Adaptive Systems too. But Bee Democracy has evolved structure and feedback mechanisms which prevent bee government from learning to create the problems it evolved to solve. The Bee Democracy structure enforces that bee politicians must earn delegation through honest debate on every proposal using information they verify for themselves.
The Human Democracy structure enforces that politicians earn delegation once by saying what they are told to say and then exploit this power for the rest of their careers. 
    * Supporting Documentation on constitutional issues
      * There must be a link from Cardano Constitution to the following document so that future generations will remember the horrors of fiat money and the central banks and never permit their return
      * [The Creature From Jekyll Island](https://drive.google.com/file/d/1Aj4rGWnTLvmXzG_gP0Xw_mM7T4Rnb3zi/view?usp=sharing)

#### **Conclusion:** 

Most all these ideas are abstracted from peer reviewed science on how bees implement democracy. Since bees have been doing it successfully for millions of years, it makes sense to consider what evolution has engineered and to use what we can. As it turns out, peer reviewed science also shows that the same methods that bees use to make decisions also evolved within the human brain. So if Cardano governance lasts long enough, the very same decision structures will likely evolve anyway. We can shorten the time it takes Cardano governance to evolve to provide the most truth and the best possible decisions for our community by studying how bee colonies and other complex adaptive systems make collective decisions.

* Links Repeated from above
* Scientific American - [You Have A Hive Mind](https://www.scientificamerican.com/article/you-have-a-hive-mind/)
* National Institute for Health - [Cross Inhibition in Collective Decision Making](https://pubmed.ncbi.nlm.nih.gov/22157081/)
* Science - [Inhibition in Collective Decision-Making](https://www.science.org/doi/10.1126/science.1210361)
* Nature - [Psychophysical Laws and the Superorganism](https://www.nature.com/articles/s41598-018-22616-y)

The process of evolution has solved many engineering problems. Bees don’t use their DReps to make decisions for the group. Bees use DReps as scouts. Bees use DReps to collect information and broadcast it to the group. Then all of them decide together. 

The Cardano protocol was built on peer reviewed science. Our community should look at peer reviewed science on how decision making has evolved in nature and apply what we can to Cardano governance.

* Links Repeated from above
* Overview - [Bee Democracy](https://youtu.be/NDnQ4pAjBUg?t=310)
* Tom Seeley, Cornell - [Details of Bee Democracy](https://youtu.be/JnnjY823e-w?t=2309)
* Tom Seeley, Cornell - [BReps vs DReps](https://youtu.be/1x8T_CHZemE?t=122)
* Tom Seeley, Cornell - [The Five Habits of Highly Effective Hives](https://youtu.be/XgSbPkInTzs?t=1929)
* 


#### **P.S.**
Ultimately, CIP-1694 is governance by jury because the Constitutional Committee must agree before governance issues are passed.  
And if IOG sponsors a proposal then they certainly have enough ADA to get it past the DRep process before passing it through the Constitutional Committee.

I don't think the designers of CIP-1694 intended to create a governance by jury system.
Rather I think they were just guided by the constraints as they worked through the problems and arrived at governance by jury (the CC) without ever intending to do it. This is the same conclusion the bees arrived at although the CC is centralized while the bees have a decentralized and randomized method of selecting the jury. I think we are already seeing natural selection at work in Cardano governance and it is already evolving towards the type of collective decision making that nature selects for.

The reason I think this is the case is because that is exactly what happened to me when trying to apply what I learned about bee governance to CIP-1694

Not every honey bee gets to vote. Only those bees (the scouts) active in collecting first hand information get the opportunity to form a quorum. This is what I was trying to apply to the representative democracy as presented in CIP-1694. Beemocracy1.0 was trying to change CIP-1694 such that ADA holders would be required to delegate on each and every governance issue that they cared about and that delegators would be able to see clearly which DReps knew the most about the governance issue and presented an onchain locked vote to receive the ADA delegation.

It quickly became clear to me that large ADA holders will have complete control of governance and that they would be incentivized to destroy the protocol for short term gains. So Beemocracy2.0 was imagined where decentralized and randomized juries would be selected based on the anonymous reputation gained through community service and tracked on chain by digital signatures. So I bumbled onto governance by jury just like the bees did. I certainly didn't design it - rather I just followed the constraints of the problem with guidance from the bees.

What just dawned on me through conversation with the community is that IOG bumbled on to governance by jury as well. The only difference is that their version has no random component and is centralized. The implication for me is that natural selection is already at work in Cardano governance and if the protocol survives long enough then it will adopt a random, centralized version of governance by jury.

Does anyone else see this unfolding?
Is CIP-1694 ultimately governance by jury or not?
If so, is there anything we can do to help decentralize the jury?
