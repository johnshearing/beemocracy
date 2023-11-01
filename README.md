# Depricated  
# [Please see Beemocracy2.0 linked here.](https://github.com/johnshearing/beemocracy/blob/main/Beemocracy2.0.md)  
[Beemocracy has been updated](https://github.com/johnshearing/beemocracy/blob/main/Beemocracy2.0.md) to reflect that all governance proposals will wind up in a jury trial anyway because of the enormously high ADA delegation threshold required for whale control. Given the above, it became obvious that it makes sense to implement Beemocracy without any mechanism to delegate ADA or count the scout votes because all proposals will ultimately be decided at jury trials anyway. This greatly simplifies the code implementation of Beemocracy and eliminates almost all of the network traffic and eliminates most of the on-chain data required to run Cardano governance.



# beemocracy1.0
Governance System For Cardano Modeled After The Democracy Which Evolved In Honey Bee Society  

Code implementation is in the planning stages  

Problems addressed:
Network traffic, Volume of data, Whale control, Privacy, Identity, Bootstrapping, Low voter turnout, Selling delegation and votes, DRep Corruption, Lack of domain expertise.

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
      * Scout bees return to the colony to report the direction and quality of a new home site with the intention of getting other scouts to examine the sight.
      * If a certain number of scouts find themselves at a new home site all at the same time (from 10 to 20 implying ≈ 150 had inspected the site) that will trigger a "quorum reaction" in the scouts which causes all of them to return back to the swarm and guide the bees to the new home site.
      * That many bees are returning to give reports on various new home sites creates a race to get new scout bees to look at the best sights in order to be the first to obtain a quorum reaction.
      * What causes bees to arrive at a quorum reaction at the most suitable new home site is:
        1. The scouts always report longer and more enthusiastically when reporting better quality sites, so more scouts will go to those sites and then return to give their own reports.
        2. No scouts will give a report without first visiting the site for themselves.
      * So honest reporting when gathering consensus using only accurate first hand information is what the structure of Beemocracy enforces.
      * [Please listen to Tom Seeley in this video](https://www.youtube.com/watch?v=1x8T_CHZemE&t=123s) which is queued up to the correct moment when he explains the difference between bee democracy and human democracy. In the video he says that no decision maker advocates for a site they have not seen for themselves whereas in human democracy the decision makers often cast votes based on affiliation without ever investigating the matter for themselves. This is the quality that Beemocracy abstracts from the collective decision making process that evolution has selected for in the honey bee colony.
    * **By abstracting nature's results into [CIP-1694](https://github.com/cardano-foundation/CIPs/tree/master/CIP-1694) we can arrive at the optimum democracy which produces the best possible decisions in the shortest amount of time**
    * A race to consensus by voting is not possible in Cardano democracy because too much network activity in a short amount of time will jam the system.
    * So deciding governance proposals at jury trials will be used to ensure that all proposals are decided based on accurate first hand information only and without breaking the network.
    * In July 2021, the Ada Lovelace Institute, working with the University of Edinburgh and the Bingham Centre for the Rule of Law, convened 50 members of the UK public in two online, week-long citizens’ juries to deliberate on and recommend good governance practice with respect to administration of health data during a pandemic. The result was definitely not the government narrative. Developed by the Jefferson Centre in the 1970s, citizens’ juries are a type of structured deliberation with members of the public, sometimes referred to as a ‘mini public’. During facilitated workshops, participants –‘the jurors’ – are given balanced information and expert presentations about a chosen issue, before deliberating on that issue and reaching a conclusion of some kind. The issue usually addresses an area of public policy, and the conclusions generated often take the form of recommendations for policymakers. That the Ada Lovelace Institute at the University of Edinburgh is experimenting with governance by jury is encouraging to me.
https://www.adalovelaceinstitute.org/report/trust-data-governance-pandemics/
  * #### Process Overview
    * Beemocracy responds to all governance proposals by inviting anyone to scout the proposal and then write a solicitation to gather ADA delegation either for or against the proposal.
    * The solicitation locks the scout's vote with a digital signature and explains in a detailed report why they voted the way they did.
    * The scout may remain anonymous and be known only by their collection of solicitations and locked votes all having the same digital signature.
    * The threshold for ADA delegation to the solicitations must be reached before the votes for a proposal will be counted.
    * The threshold for ADA delegation must always be set very very high to ensure that everyone in the community is represented, not just the whales.
    * The threshold for ADA delegation will rarely if ever be reached unless the proposal really really matters to the common folks who wish to prevent a decision at a jury trial and rather decide the proposal directly. The result is, proposals will rarely if ever be decided by delegation and so ADA holders will learn they don't need to delegate their ADA in order to get good governance decisions. So there is no network traffic except to register a scout's solicitation for or against a proposal and to lock their vote.
    * When the ADA delegation threshold for a proposal is not reached before a set time (as expected) then the proposal will go before a jury of randomly selected scouts who have submitted at least 10 solicitations within the past 365 days. These 10 digitally signed solicitations with locked votes are used by the prosecution and the defense to evaluate the character of the scouts during jury selection. Prosecution and defense will alternate selections from a random pool of eligible scouts based on previous solicitations and some standard questions asked by the judge. If a scout is selected to serve on the jury and has written a solicitation on the matter with an associated locked vote then the locked vote is not binding. The scout is free to listen to all arguments and decide anew. Locked votes are only binding if the delegation threshold is reached in which case the matter has already been decided by the locked votes as weighted by delegation of ADA.
    * So the only reasons for putting an issue up for vote are to:
      1.  Get a body of solicitations for or against the governance proposal that the scout jury can use in deciding.
        * Think scout bees examining various sites for their new hive.
        * Think scouts coming back to the hive for a waggle dance debate with **first hand information** to use in making a decision.
      2.  Create a large educated jury pool of scouts who are invested by their anonymous reputation earned in the solicitation process.
        * Think a guaranteed quorum of interested and invested decision makers with first hand information to work with.
    * Given the above, it might well be better to implement Beemocracy without a mechanism to delegate ADA or count the scout votes because all proposals will ultimately be decided at jury trials anyway.
      * This will greatly simplify the implementation of Beemocracy and eliminate almost all of the network traffic and eliminate most of the data too.
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
      * #### BReps (the scouts) compete for delegation with no reward except for the survival and prosperity of their hive which includes their own survival and prosperity
        * If paying scouts for their work produced more truth than simply working for their own survival and prosperity then evolution would have selected for that
      * Bee democracy is structured like so because those structured differently were all selected out of existence
      * Cardano Democracy cannot be modeled on Human Democracy without becoming a selfish monster that self-destructs over time just like all the others. But if IOG abstracts the structure and feedback mechanisms found in Bee Democracy and applies these to Cardano Democracy then we will have governance that does not learn to create the very problems it was built to solve in order to feed and grow. Evolution already did the research. All we need to do is look at what the bees are doing. We should model Cardano governance on Bee Democracy -  the one which nature has perfected over the course of millions of years  
    * #### **Abstracting bee democracy functions and applying these to Cardano governance**
      * The data structure of this governance system is much like any online forum that we are used to.  
      * The governance is hosted on an immutable online forum for:
        *  Submitting and reading governance proposals 
        *  Submitting and reading BRep opinions, debate and votes
        *  Delegating ADA to the delegation options for the proposal (For | Against | Abstain)
      * Each BRep must solicit for delegation on each and every proposal they wish to weigh in on using an online document (a solicitation) which explains their position and which also locks their vote. 
      * The mechanism is an on-chain transaction with a signed vote and the hash of the solicitation text on an immutable webpage.
      * The URL for any webpage on the Interplanetary File System (IPFS) is the hash of the webpage text.
        * So the on-chain transaction with the signed vote and hash of the solicitation text points to the solicitation text on the IPFS forum webpage.  
      * The BRep's vote is cast and embedded in the solicitation text with their digital signature. 
      * The BRep's vote can not be changed once the solicitation has been published, so delegators know what they are getting.
      * Delegators delegate ADA to the BRep's solicitation rather than to the BRep directly.  
      * Delegators choose: Delegation of their ADA either adds to the weight of a solicitation vote, reduces the weight of a solicitation vote, or adds to the weight of the abstain option for the original proposal. Then the weights of all solicitations for a proposal are summed to decide the election. It is best that delegators can also delegate directly to the proposal itself either for, against, or abstain. This way if no other solicitation is written then delegators can still delegate for or against the proposal. What that really means is that each proposal is actually a solicitation too - the proposal itself is also the first solicitation for delegation in support of the proposal.
      * Delegators may change their delegation at any time before the final tally
      * Delegators may not vote directly, rather delegators may register as a BRep and then delegate ADA to their own solicitation vote. 
      * Governance System Structure In More Detail
        * The original governance proposal is also the first solicitation for delegation.
          * The hash of the solicitation text goes on chain in a transaction along with the signed BRep vote in support of his/her proposal.
          * The hash of the solicitation text is also the URL of the document when posted using the IPFS protocol.
          * So the vote on the Cardano blockchain is linked to the text of the proposal (1st solicitation) on the IPFS webpage.
          * Delegators may delegate directly to this first solicitation: For | Against | Abstain.
        * Other BReps may wish to comment and vote on the proposal and delegators may delegate their ADA to the comment and signed vote of the BRep that makes sense to them.
          * BReps will write solicitations of their own with respect to the original proposal asking for delegation to support their vote: For | Against | Abstain.
          * The voting transaction is assembled as follows:
            * The vote (For | Against | Abstain) is included in the transaction.
            * The text of these solicitations are hashed and included in the voting transaction.
              * Again, this hash is also the URL of the webpage that holds the solicitation text.
            * The supporting solicitations also have another field in the on chain transaction which is just the hash/URL of the original proposal.
              * This establishes the new solicitations as children of the original proposal.
              * So it is easy make a webpage that links the original proposal/solicitation with all the children solicitations underneath.
              * Delegators can delegate to the original proposal (For | Against | Abstain) or they can delegate to any of the children solicitations.
              * All the ADA delegation (For | Against | Abstain) is summed to decide the election.
        * Linking Comments Where BReps Can Show They Changed Their Mind Even If They Can't Change Their Vote.
          * These would be a signed on chain transaction with the hash of the retraction text, or hash of additional comment.
            * This serves as the IPFS URL and makes it impossible to tamper with the text. 
            * Another field in the transaction is the hash of the BReps solicitation for which they now wish to comment on.                  
            * This establishes exactly what previous solicitation they are commenting on.
            * This makes the retraction a child of the BRep's solicitation and the solicitation is a child of the original proposal.
            * So now the retraction gets listed under their voting solicitation and delegators can see that the BRep now regrets the vote.
          * It is important that the BReps not be able to change their vote because people agreed with the original reasoning in the solicitation and delegated accordingly.
            * And just because the BRep has had a change of mind does not mean that the delegators will also.
            * This is one of the biggest differences between CIP-1694 and Beemocracy:
            * With CIP-1694 delegation stays with the DRep no matter how they swing.
            * With Beemocracy, delegation is linked to the reasoning in the BReps appeal for delegation to their vote.
            * DReps are elected rulers.
            * BReps are scouts which collect and share information so that the community can make good collective decisions.
      * After each election is over, the forum webpage for each governance proposal will show aggregated votes and delegations for the solicitations so as to provide an audit trail for every governance proposal election.  
        * #### We will need filtering tools in our blockchain explorers to help forum operators organize the volume of solicitations. 
        * [Voting Tools - RS](https://github.com/input-output-hk/voting-tools-rs) by IOG might be that tool.
        * #### Actual voting and aggregation will be done using zero knowledge proofs with Mithril on the Midnight sidechain.
          *  This is to:
          *  Protect the anonymity of the voters
          *  Provide each voter with mathematical proof that their vote was cast as desired.
          *  Provide the community with mathematical proof that the aggregated results are correct.
          *  Prevent information leakage of election results before voting is completed.
            * This suppresses a market for votes and delegation and prevents early results from affecting the votes. 
      * #### Staking To Pay For the Immutable Website Which Hosts the Online Forum For Governance Proposals, Solicitations, Debate, Voting, And Delegation 
        * We will need an immutable website using the decentralized IPFS protocol which presents a forum to contain the text and the hash for all governance proposals and all BRep solicitations for delegation, for or against the proposal. 
        * Everything on the governance website must persist for all eternity so future generations will know why we made the decisions we made.
        * With every governance proposal and solicitation, there must be a payment in ADA to cover the cost of hosting the proposal and to prevent spamming the system.
        * This ADA will be staked in a random stake pool, and automatically, the staking rewards will be distributed to the owners of the computers which host the proposal webpages by lottery as follows.
          * Distributing the staking rewards by lottery allows market forces to promote redundant copies of all proposal webpages.
          * At random intervals, one of the hosted webpages (selected by lottery) for a given proposal will be requested and hashed to ensure the data is accessible and that the contents has not been altered.
          * The IPFS address and the document hash should be the same if the document has not been changed.
          * If the proposal webpage is returned unaltered then the host is paid the staking rewards associated with that lottery slot
          * If the proposal webpage is not returned by the host computer then the host does not get paid the lottery reward and the lottery is repeated with another host for that proposal webpage selected at random.
          * If a host fails again to return the data the next time it wins the lottery then it is removed from the index of hosts for that governance proposal
          * So document hosts get paid by lottery in much the same way as Cardano stake pool operators get paid
        * In this way the proposal webpage and all associated solicitations will persist for all eternity in a decentralized manner.
        * It may be that the cost of bandwidth and hashing power are too expensive to allow verification for proof of bandwidth and proof of storage. It is my understanding that currently the consumer/tester must request the entire document, and the host must provide it in a timely manner. Then the consumer/tester must hash the document to ensure that it matches the IPFS address of the document. This may be prohibitively expensive and is perhaps one reason that decentralized document storage has not caught on despite all the money which has been spent developing the idea. One compromise which proves the host at least has the document is to send the host a random number that is to be appended to the document. The host then hashes the document and sends back the hash to the consumer/tester. This requires much less bandwidth. Then the consumer/tester hashes the document along with the same appended random number. If the hash is the same then the consumer/tester knows that the host at least is in possession of the document. The problem with this approach is that the consumer/tester must also have the document in order to hash it, and the hashing computation is expensive and so is the bandwidth required to get the document from the host. I am no expert, in fact I am not even a novice, but it seems to me that recursive zero knowledge proofs, which will likely be available with the Midnight sidechain, solve this problem and so Cardano could be the first to market with an inexpensive way to prove a host at least is in possession of a document. Then reports from general consumers could be used to verify bandwidth and document availability.
      * CC, BRep, and SPO votes to remain transparent by virtue of the solicitation process which forces all to explain their votes and leave a body of information so that future generations will understand why those decisions were made
      * **The Bee Democracy Structure Ensures That:**  
        * Delegators have lots of good information to make their decisions  
        * Delegators are deliberately casting their delegation of ADA for a given proposal via solicitations
        * Uninformed delegators don't delegate  
        * Uninformed BReps don't vote
        * Delegators know in advance, before delegation, how BReps voted and why
        * BReps must explain their reasoning on every proposal
        * A body of literature remains (the solicitations) so future generations will understand how we came to our decisions and what they should consider before making changes
        * Votes and delegations are bound to solicitations for or against a proposal as an audit trail of the election and proof that there has not been any election fraud.
        * #### BReps can remain anonymous, building reputations only on their body of solicitations which all have the same signature.  

#### **Prevent Buying and Selling of Delegation** 
 * With regard to [CIP-1694](https://github.com/cardano-foundation/CIPs/tree/master/CIP-1694), Treasury withdrawals come to mind but there will be a market for delegation on most any governance action. It seems that in a close election where there is a lot of ADA waiting on the outcome, a market for delegation is created where delegation becomes much more valuable as we approach the [end of an epoch](https://github.com/cardano-foundation/CIPs/tree/master/CIP-1694#lifecycle) when votes are tallied. Payment for delegators could be in ADA or another currency. So there may be a perverse incentive for delegators to wait till the last minutes of an epoch before delegating in order to get the best price for their delegation. Aside from corrupting the election, it could also overload the system as votes come in at the last moments before an epoch closes.
  * There is already an automated market for buying and selling delegation on Catalyst proposals [as seen in the video linked here](https://www.youtube.com/live/qhG2EiFJrRk?feature=share&t=1472) which is queued up to the spot where it is explained what they are doing. Many may be shocked to know that this is happening already and that there is no reason the same scheme cannot be perpetuated against governance in CIP-1694. The way I see it, only thing that will protect the community from having the treasury emptied or the parameters hijacked as CIP-1694 stands now is the constitutional committee.
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
        * Protects delegator from reprisal by a current regime  
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
        * That this is possible with zero knowledge proofs seems like magic to me so I am working now to verify that this is indeed possible. If it is then everything else is just a matter of coding. It will not be an easy task but IOG has provided the tech stack and the learning tools so I am just going to do it a step at a time. Maybe others will want to help or perhaps will want to compete with their own implementation. The Cardano blockchain is permissionless so there is no limit to the amount of governance systems that can live and work on the Cardano blockchain. So we might as well try a lot of different ideas - it's all good for the community. I intend to build a governance system modeled on Bee Democracy.
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
    * #### **Putting A Proposal On Trial**
      * If an election does not meet the threshold for delegator participation then the proposal goes to trial. 
      * Jurors are randomly selected from the pool of BReps in an amount equal to the number of Constitutional committee members. Their identities are not required - they can remain anonymous. All that is required is that they have submitted perhaps 10 solicitations in the past 365 days. If they can provide the same signature that is on their past solicitations, that is all which is needed to establish them as community members and to judge their character and reputation.
      * In an online meeting (audio only - no video), each juror is questioned by BReps from both sides of the proposal to determine that they are willing to examine both sides of the issue and have the time to do so.
      * Jurors are then asked to read the solicitations. 
      * The next day there is a group online discussion with BReps from both sides of the proposal presenting to the jurors
      * Finally, the jurors vote on the proposal using the same signature they have been using to sign their past solicitations
    * Advantages of the Trial Structure For Handling Low Delegator Turnout
      * **Cardano Citizens remain anonymous and yet establish their BRep identity, reputation and right to vote in trials through their work creating solicitations**.
        * This is a big deal. This is the closest we can get to establishing a one person one vote system without the need to know the identities of our citizens.
        * This works because BRep identities are established by the digital signatures on their solicitations which are the same signatures they use to vote in trials.
      * **Boot Strapping Problem is solved**.
        * All citizens have the right to delegate their ADA to a BRep's solicitation and any citizen can become a BRep and write a solicitation that receives delegation. But only BReps that have created a body of 10 or more solicitations in the past 365 days are eligible to vote in a trial. So all governance actions are first presented as solicitations that the entire community votes on by virtue of their delegation to the solicitations. In the beginning, if delegator turn out is low then the proposal goes to trial and the Constitutional Committee will vote on the matter. But while these first 10 governance actions are being decided, BReps are establishing their anonymous identities, reputation, and right to vote in trials by writing their own solicitations. In only a short time, the community will have a very large pool of BReps that have earned the right to vote on proposals that go to trial. At this point the Constitutional Committee is no longer involved in proposal trials and decide only whether or not proposals are constitutional. By putting all proposals before the entire community first, we insure that many more citizens are continually writing BRep solicitations and earning their right to vote in trials.
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

**Conclusion:** 

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
