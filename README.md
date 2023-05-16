# beemocracy
Voting System For Cardano Modeled After The Democracy Which Evolved In Honey Bee Society  

Code implementation coming soon  

Problems addressed:
Privacy, Identity, Bootstrapping, Low voter turnout, Selling delegation and votes, DRep Corruption, Lack of domain expertise.

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
      * Newsweek - [Bee Colonies Behave Like the Human Brain](https://www.newsweek.com/bee-colonies-behave-human-brain-study-finds-863576)
      * Nature - [Psychophysical Laws and the Superorganism](https://www.nature.com/articles/s41598-018-22616-y)
    * Given enough time, Cardano governance will likely evolve the same structure. 
    * **By abstracting nature's results into [CIP-1694](https://github.com/JaredCorduan/CIPs/blob/voltaire-v1/CIP-1694/README.md) we can arrive at the optimum democracy which produces the best possible decisions in the shortest amount of time** 
  * #### Bee Democracy
    * Bee Democracy has DReps. Let's call them BReps. 
    * These are the scouts which return to the hive with information about a particular proposal (A new location for the hive)
    * From the video we see that BReps dance for the delegators to communicate why their proposal is the best.
    * Unlike our DReps...
      * The Bee Democracy structure enforces that BReps must earn delegation through honest debate using information they verify for themselves. The result is good decisions.
        * The Human Democracy structure has no means to enforce that DReps debate nor is there any means to ensure they make decisions based on information they have verified for themselves. The result is echo chambers, information bubbles, ignorance, hysteria, cronyism, and ultimately very bad decisions.
      * BReps only receive delegation for the proposal they are currently soliciting for - Then delegation ends
        * This is key to a functioning democracy - DReps in the bee's world have to earn their delegation for each proposal
        * In human democracy the DReps only their earn delegation once and then learn to exploit their power for personal gain during the rest of their careers
      * BReps (the scouts) compete for delegation with no reward except for the survival and prosperity of their hive which includes their own survival and prosperity
        * If paying scouts for their work produced more truth than simply working for their own survival and prosperity then evolution would have selected for that
      * Bee democracy is structured like so because those structured differently were all selected out of existence
      * Cardano Democracy cannot be modeled on Human Democracy without becoming a selfish monster that self-destructs over time just like all the others. But if IOG abstracts the structure and feedback mechanisms found in Bee Democracy and applies these to Cardano Democracy then we will have governance that does not learn to create the very problems it was built to solve in order to feed and grow. Evolution already did the research. All we need to do is look at what the bees are doing. We should model Cardano governance on Bee Democracy -  the one which nature has perfected over the course of millions of years  
    * #### **Abstracting bee democracy functions and applying these to Cardano governance** 
      * Each BRep must solicit for delegation on each and every proposal using an online document (a solicitation) which explains their position and which also locks their vote. 
      * The mechanism is an on-chain transaction with a signed vote and the hash of an immutable webpage which contains the solicitation text.
      * The URL for any webpage on the Interplanetary File System is the hash of the webpage text.
        * So the on-chain transaction with the signed vote points to the solicitation text on the IPFS.  
      * The BRep's vote is cast and embedded in the solicitation with their digital signature. 
      * The BRep's vote can not be changed once the solicitation has been published so delegators know what they are getting.
      * Delegators delegate ADA to the BRep's solicitation rather than to the BRep directly.  
      * Delegators choose: Delegation of their ADA either adds to the weight of a solicitation vote, reduces the weight of a solicitation vote, or adds to the weight of the solicitation abstain option. Then the weights of all solicitations for a proposal are summed to decide the election. It is best that delegators can also delegate directly to the proposal itself either for, against, or abstain. This way if no solicitation is written then delegators can still delegate for or against the proposal. What that really means is that each proposal is actually a solicitation too - the proposal itself is also the first solicitation for delegation in support of the proposal.
      * Delegators may change their delegation at any time before the final tally
      * Delegators may not vote directly, rather Delegators may register as a BRep and then delegate ADA to their own solicitation if they wish and then vote on that. 
      * We will need filtering tools in our blockchain explorers to help delegators make sense of the volume of solicitations. [Voting Tools - RS](https://github.com/input-output-hk/voting-tools-rs) by IOG might be that tool.
      * We will need an immutable website (perhaps on IPFS) that uses a forum format much like we have here to contain the text and the hash for all governance proposals and all BRep solicitations for delegation, for or against the proposal. The webpage for each governance proposal will aggregate the votes and delegations on the solicitations so as to provide an audit trail for every governance proposal election.
      * CC, BRep, and SPO votes to remain transparent by virtue of the solicitation process which forces all to explain their votes and leave a body of information so that future generations will understand why those decisions were made
      * Code to enforce that delegation of ADA to a solicitation must come from a wallet and never from a smart contract
        * This is to prevent trustless renting of ADA via smart contract for use as delegation in an election
        * In other words to rent out ADA for use as delegation, the renter will be forced to give up custody
      * **The Bee Democracy Structure Ensures That:**  
        * Delegators have lots of good information to make their decisions  
        * Delegators are deliberately casting their delegation of ADA for a given proposal via solicitations
        * Uninformed delegators don't delegate  
        * Uninformed BReps don't vote
        * Delegators know in advance, before delegation, how BReps voted and why
        * BReps must explain their reasoning on every proposal
        * A body of literature remains (the solicitations) so future generations will understand how we came to our decisions and what they should consider before making changes
        * Votes and delegations are bound to solicitations for or against a proposal as an audit trail of the election and proof that there has not been any election fraud.
        * BReps can remain anonymous, building reputations only on their body of solicitations which all have the same signature.  

#### **Prevent Buying and Selling of Delegation** 
 * With regard to [CIP-1694](https://github.com/JaredCorduan/CIPs/blob/voltaire-v1/CIP-1694/README.md), Treasury withdrawals come to mind but there could be a market for delegation on most any governance action. It seems that in a close election where there is a lot of ADA waiting on the outcome, a market for delegation is created where delegation becomes much more valuable as we approach the [end of an epoch](https://github.com/JaredCorduan/CIPs/blob/voltaire-v1/CIP-1694/README.md#lifecycle) when votes are tallied. Payment for delegators could be in ADA or another currency. So there may be a perverse incentive for delegators to wait till the last minutes of an epoch before delegating in order to get the best price for their delegation. Aside from corrupting the election, it could also overload the system as votes come in at the last moments before an epoch closes. 
  * Delegation is linked to wallets in an obvious way so payment for delegation could be most easily made in ADA.  
  * In this market for delegation:  
    * Where it is known exactly how much delegation you still need in order to get the ADA for your project out of the treasury,  
    * which makes possible to calculate with certainty the price for delegation which leaves you with your target profit margin intact,  
    * and where you can broadcast an offer to purchase delegation,  
    * and where you can see exactly which wallets are delegating to you in response to your offer...  
    * Then you know exactly where to send the delegator's share of ADA after snatching it from the treasury.  
    * Likely this fraud could be automated via smart contract in a trustless manner such that the price for  delegation is displayed and so that the dishonest delegators would not need to trust the dishonest DRep for payment.  
    * This attack could also be carried out on a vote for parameter change or on any other governance action.  
  * In bee democracy there is a race to consensus which prevents a market for delegation from emerging - Bees can't sell their delegation 
    * A race to consensus is not possible in Cardano democracy because too many votes or delegations in a short amount of time will jam the system
    * So other methods must be employed to make delegation of ADA more costly to buy then simply buying ADA at market rate.  
      * Block the ability to read the total amount of ADA delegated to a BRep's solicitation while voting is in progress.  
        * This makes it impossible to calculate the ADA tally until the election is over
        * This will help prevent a delegation market from emerging during an election by making it difficult to determine how much ADA delegation is required to pass a proposal  
        * This may necessitate voting on a sidechain which has the required properties 
      * Block the ability of anyone except the delegator from seeing to which solicitation an individual has delegated   
        * This will help prevent a delegation market from emerging during an election by making it difficult to determine the how much ADA is needed to pass a proposal
        * Prevents a delegation market from forming because it would not be easy (cost effective) for BReps to know where to send ADA in exchange for delegation after the election  
        * Prevents automating a delegation market with smart contracts
        * Allows proof that an election is not rigged  
        * Protects delegator from reprisal by current a regime  
        * This may necessitate voting on a sidechain which has the required properties
      * #### **The voting mechanism is generally as follows:**
        * The functionality described can be built into any Cardano wallet to make the delegating experience quick and easy:
        * Using the browser embedded into the wallet, the delegator visits the Interplanetary File System (IPFS) website where Cardano proposals are hosted.
        * The delegator navigates to the desired proposal and reads it.
        * The proposal is the first solicitation so if the delegator thinks they have enough information then they can delegate (for | against | abstain) by the method to be described shortly.
        * If the delegator would like to know more before delegating then they can read the solicitations (for, against, abstain) written by BReps which are webpages  found by links below the proposal. 
        * If any of these opinions resonate with the delegator then they can delegate to the solicitation (for | against | abstain) by the following method:
          * The IPFS URL of the solicitation webpage is the hash of the webpage and the hash of the webpage is one of the fields in the Cardano transaction which registers the solicitation. So the wallet finds the solicitation transaction_ID on the Cardano blockchain using the webpage URL as the key.
          * Now, using the wallet, the user chooses to delegate (for | against | abstain)
          * Next the user pushes the sign the transaction button and a zero knowledge proof is generated. This proves that a user delegated their wallet to their selected solicitation with their selected (for | against | abstain) option but will not reveal any of this information at this time
          * Then the wallet encrypts the signed transaction with a public key generated by the Constitutional Committee. This way, no one will be able to see the zero knowledge proof until it's time to count the votes. Hiding the delegation count until the election is over will help to suppress a market for selling delegation. Does Mithril have a use here?
          * Now the wallet broadcasts the transaction and receives a receipt which can be applied to a zero knowledge proof verifier so that the wallet owner can verify that their delegation was cast correctly. 
          * After the voting deadline is over. Constitutional Committee takes a snapshot of the blockchain to see how much ADA each wallet contains and then decrypts the zero knowledge proofs of how the wallets were delegated so as to see how much ADA was delegated (for | against | abstain) with respect to the proposal all without ever exposing which wallets were delegated to the solicitations. 
        * That this is possible with zero knowledge proofs seems like magic to me so I am working now to verify that this is indeed possible. If it is then everything else is just a matter of coding. It will not be an easy task but IOG has provided the tech stack and the learning tools so I am just going to do it a step at a time. Maybe others will want to help or perhaps will want to compete with their own implementation. The Cardano blockchain is permissionless so there is no limit to the amount of voting systems that can live and work on the Cardano blockchain. So we might as well try a lot of different ideas - it's all good for the community. I intend to build a voting system modeled on Bee Democracy.
        * #### **The Tool Stack**
          * [Voteaire](https://voteaire.io/) is a functioning voting system which runs on Cardano
            * Congratulations to the Voteaire Team! 
            * The Voteaire Team has agreed to see what they can do to help with this project
          * [Mina - A Zero Knowledge Proof Blockchain](https://minaprotocol.com/)
            * Mina uses Cardano's Ouroboros consensus mechanism but replaces the blockchain with a recursive zero knowledge proof
            * The proof always remains the same small size - about 22KB
            * [Dr Vanishree Rao, formerly of Mina, is now Head of Applied Cryptography at IOG](https://www.bitcoininsider.org/article/192150/academic-who-led-mina-protocol-development-joins-cardano-builder-iog-head-applied)
              * This tells me we should be looking at Mina to see what ZKP tool stack is likely to work with Cardano moving forward.
             * See Mina's blog post: [Zero-Knowledge Proofs for Voting](https://blog.o1labs.org/zero-knowledge-proofs-for-voting-3c6a6d5d89db)
            * [Here we see](https://youtu.be/KVJWBk0wNSE?t=46) it is possible to experiment with Mina and later add our own ZK application layer to Cardano when we know more about what we need.
          * IOG is developing the following tools which relate to voting or use ZKPs
            * [Mithril](https://mithril.network/doc/)
              * Cardano's own Mithril project seems promising for exactly this type of voting [as seen in this video linked here](https://youtu.be/MlBipDc6GPU) presented by ADA North Pools
                * It seems the function of Mithril is to allow multiple parties (scales to thousands) to sign a transaction anonymously in such a way that the amount of ADA they hold is weighted in the signature. That's exactly what is required in order to implement a voting system which weighs solicitations according to delegation while ensuring privacy.
              * Mithril uses [Bulletproofs](https://github.com/sdiehl/bulletproofs) (zero knowledge proofs written in Haskell) as seen [in this video](https://youtu.be/MlBipDc6GPU) also presented by ADA North Pools.
            * [IOG's Voting Tools - Rust](https://github.com/input-output-hk/voting-tools-rs)
              * This tool generates voting power info from a db-sync instance.
            * [Cardano Sidechains Tooling](https://github.com/input-output-hk/sidechains-tooling)
            * [Atala Prism](https://atalaprism.io/)
            * Midnight
              * Cardano's privacy coin under development
            * [Kachina](https://iohk.io/en/research/library/papers/kachina-foundations-of-private-smart-contracts/)
              * Cardano's privacy smart contracts under development
          * IOG has the following blog posts and papers on the related to voting and ZKPs: 
            * [Zk-SNARKs: updatable setups on the blockchain](https://iohk.io/en/blog/posts/2022/09/01/zk-snarks-updatable-setups-on-the-blockchain/) 
            * [ATreasurySystemforCryptocurrencies: Enabling Better Collaborative Intelligence](https://eprint.iacr.org/2018/435.pdf)
            * [Mithril: Stake-based Threshold Multisignatures](https://iohk.io/en/research/library/papers/mithril-stake-based-threshold-multisignatures/)
            * [Decentralised Update Selection with Semi-Strategic Experts](https://iohk.io/en/research/library/papers/decentralised-update-selection-with-semi-strategic-experts/)
            * [Privacy Preserving Opinion Aggregation](https://iohk.io/en/research/library/papers/privacy-preserving-opinion-aggregation/)
            * [Models for Generation of Proof Forest in ZK-SNARK Based Sidechains](https://iohk.io/en/research/library/papers/models-for-generation-of-proof-forest-in-zk-snark-based-sidechains/)
          * Learning materials for working with ZKPs are [found at this link here](https://github.com/matter-labs/awesome-zero-knowledge-proofs)
            * Thanks to PREEB Pool for [information about the learning materials](https://cardano.stackexchange.com/questions/11083/preferred-library-for-working-with-zero-knowledge-proofs/11084#11084)

#### **Dealing With Low Delegator Participation Which Blocks Governance Action**  
  * It is essential for the security of the Cardano blockchain that delegators (the regular folks) participate in elections. Otherwise whales and exchanges will be winning all the governance actions and will manipulate Cardano government for their advantage with little or no consideration for the unbanked individuals that Cardano was built to serve. It is assumed that the big investors will always delegate their ADA to any solicitation which best advances their goals. Since it can be estimated how much ADA is held by big investors, a delegation threshold parameter is coded into the system to ensure that a significant amount of ADA (well above what the big investors hold) is delegated to the solicitations. This is the only way to know for sure that the little people are delegating too. If delegation to the solicitations does not meet the threshold when votes are tallied then the proposal is dismissed and no action is taken. So a mechanism which is meant to protect small investors will have the unintended consequence of blocking all governance if small investors are not interested enough to delegate their ADA in order to settle the matter. There is a way to proceed with governance if a proposal suffers from low delegator participation
    * **Putting A Proposal On Trial**
      * If an election does not meet the threshold for delegator participation then the proposal goes to trial. 
      * Jurors are randomly selected from the pool of BReps in an amount equal to the number of Constitutional committee members. Their identities are not required - they can remain anonymous. All that is required is that they have submitted perhaps 10 solicitations in the past. If they can provide the same signature that is on their past solicitations, that is all which is needed to establish them as community members and to judge their character and reputation.
      * In an online meeting (audio only - no video), each juror is questioned by BReps from both sides of the proposal to determine that they are willing to examine both sides of the issue and have the time to do so.
      * Jurors are then asked to read the solicitations. 
      * The next day there is a group online discussion with BReps from both sides of the proposal presenting to the jurors
      * Finally, the jurors vote on the proposal using the same signature they have been using to sign their past solicitations
    * Advantages of the Trial Structure For Handling Low Delegator Turnout
      * **Cardano Citizens remain anonymous and yet establish their BRep identity, reputation and right to vote in trials through their work creating solicitations**.
        * This is a big deal. This is the closest we can get to establishing a one person one vote system without the need to know the identities of our citizens.
        * This works because BRep identities are established by the digital signatures on their solicitations which are the same signatures they use to vote in trials.
      * **Boot Strapping Problem is solved**.
        * All citizens have the right to delegate their ADA to a BRep's solicitation and any citizen can become a BRep and write a solicitation that receives delegation. But only BReps that have created a body of 10 or more solicitations are eligible to vote in a trial. So all governance actions are first presented as solicitations that the entire community votes on by virtue of their delegation to the solicitations. In the beginning, if delegator turn out is low then the proposal goes to trial and the Constitutional Committee will vote on the matter. But while these first 10 governance actions are being decided, BReps are establishing their anonymous identities, reputation, and right to vote in trials by writing their own solicitations. In only a short time, the community will have a very large pool of BReps that have earned the right to vote on proposals that go to trial. At this point the Constitutional Committee is no longer involved in proposal trials and decide only whether or not proposals are constitutional. By putting all proposals before the entire community first, we insure that many more citizens are continually writing BRep solicitations and earning their right to vote in trials.
      * **The community gets first shot at handling all governance actions**
      * **The community can take control from the BReps at any time simply by delegating**
        * Because all proposals go before the delegators (the regular folks) first before going to trial, delegators can take all power away from the BReps simply by turning out for delegation to the solicitations. If delegators reach the threshold for delegations then the BReps never get to vote on the proposal in a trial. Power to the people! That's incentive to delegate.

#### **Constitutional Issues**
  * Decentralization Alone Can't Stop Cardano Governance From Becoming Like The Central Banks.
    * **Constitutional Amendments Required:**
      * **The Free Market Will Determine The Price Of ADA**
        * The price of ADA will not be set in relation to any other commodity nor any other currency by any authority. 
      * **No Oracles Will Be Used To Decide Any Governance Issues** 
        * Community members are responsible for determining what is true and expressing it with solicitations, debate, votes, and delegation
        * The free market will determine prices - not oracles
      * **ADA To Be The Only Form Of Currency Accepted Into The Treasury**
        * No receipt money shall be accepted into the treasury: 
          * Receipt money means you get a receipt for a commodity being held somewhere presumed to be safe
          * History shows that all banks will eventually succumb to the temptation of lending out the commodity backing the receipt, either in secret or publicly as fractional reserve banking.
          * This started in the middle ages when goldsmiths would hold gold in their safe for customers and provide a receipt which could be redeemed for the gold. Eventually the receipt became accepted as payment for commodities. But the goldsmiths would always lend out the gold to gain interest without telling the owners and would eventually default when the community discovered, leaving the customers with nothing. The most recent example of commodity-backed money was the US dollar which up until 1933 could be redeemed for gold at at $20.67 per troy ounce. Then it transitioned to fractional money when the price was changed to $35 per ounce in 1934, effectively reducing the value of the dollar by almost 41%. Then it transitioned to fiat money in 1971 - not redeemable for anything, but which citizens are required by law to accept. This is not the exception, this is the absolute rule. All commodity-backed money is a commodity in transition to fiat money. My understanding is that history has no exceptions to this rule. This information comes from [The Creature From Jekyll Island.pdf](https://drive.google.com/file/d/1Aj4rGWnTLvmXzG_gP0Xw_mM7T4Rnb3zi/view?usp=sharing). The transition may take several years but history shows that commodity-backed money always transitions to fiat money eventually. This has been going on since the middle ages and we now stand in a place where we can stop it.
        * No Stable Coins shall be accepted into the treasury
          * Stablecoins are just commodity or fiat backed overcollateralized receipt money in a new slick package. We have all seen what happens to stablecoins. Worse, all stablecoins that I know of are centralized money and require an oracle to function. So if spending requires using a stablecoin then the exchange must occur at the point of sale. Forbidding centralized currency forbids stablecoins and receipt money and commodity-backed and overcollateralized money. But we should forbid these explicitly. One thing we can not do is accept commodity-backed and overcollateralized money and stablecoins and then forbid centralized money because this is a contradiction - these are all centralized money.
        * No Algorithmic Stable Coins shall be accepted into the treasury
          * With Djed for example, we hear from Shahaf Bar-Geffen who is the COTI CEO that [Djed may be colateralized with a basket of different coins not just ADA](https://youtu.be/PipEUycQwfA?t=978). Another coin called Shen is already used in the process. I can't find much out about Shen - I don't know if it is a blockchain or a DAG like COTI. Further more, Djed is pegged to the dollar. So if you put $20 ADA in to the contract then you get $20 of Djed minus a fee for the exchange. When you want to cash out then you give your Djed back and get your $20 dollars worth of ADA back minus fees again. But what about inflation? Your $20 minus the fees is worth less because of inflation. So you suffer a loss because the dollar will be worth less when you go to get your ADA back. And if the dollar tanks then you are really in bad shape. Another concern is that Coti was associated with Ardana, and we all know how that went. Seems like the only reason to hold Djed in the Cardano treasury is if you think the price of ADA is going to fall. Does Cardano want to bet against itself? Reminds me of The Big Short. With all these questions about Djed and with all the bad history we have with stable coins it seems we should explicitly forbid holding them in the treasury.
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

**Conclusion:** 

Most all these ideas are abstracted from peer reviewed science on how bees implement democracy. Since bees have been doing it successfully for millions of years, it makes sense to consider what evolution has engineered and to use what we can. As it turns out, peer reviewed science also shows that the same methods that bees use to make decisions also evolved within the human brain. So if Cardano governance lasts long enough, the very same decision structures will likely evolve anyway. We can shorten the time it takes Cardano governance to evolve to provide the most truth and the best possible decisions for our community by studying how bee colonies and other complex adaptive systems make collective decisions.

* Links Repeated from above
* Scientific American - [You Have A Hive Mind](https://www.scientificamerican.com/article/you-have-a-hive-mind/)
* National Institute for Health - [Cross Inhibition in Collective Decision Making](https://pubmed.ncbi.nlm.nih.gov/22157081/)
* Science - [Inhibition in Collective Decision-Making](https://www.science.org/doi/10.1126/science.1210361)
* Newsweek - [Bee Colonies Behave Like the Human Brain](https://www.newsweek.com/bee-colonies-behave-human-brain-study-finds-863576)
* Nature - [Psychophysical Laws and the Superorganism](https://www.nature.com/articles/s41598-018-22616-y)

The process of evolution has solved many engineering problems. Bees don’t use their DReps to make decisions for the group. Bees use DReps as scouts. Bees use DReps to collect information and broadcast it to the group. Then all of them decide together. 

The Cardano protocol was built on peer reviewed science. Our community should look at peer reviewed science on how decision making has evolved in nature and apply what we can to Cardano governance.

* Links Repeated from above
* Overview - [Bee Democracy](https://youtu.be/NDnQ4pAjBUg?t=310)
* Tom Seeley, Cornell - [Details of Bee Democracy](https://youtu.be/JnnjY823e-w?t=2309)
* Tom Seeley, Cornell - [BReps vs DReps](https://youtu.be/1x8T_CHZemE?t=122)
* Tom Seeley, Cornell - [The Five Habits of Highly Effective Hives](https://youtu.be/XgSbPkInTzs?t=1929)
