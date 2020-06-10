# quadraticOcean

This is a work in progress, as I found out about this hackathon a bit late. I hope to submit more of my ideas and some working versions of an interface.

Thanks for taking the time to check this out!


Quadratic Voting is most useful in cases where there are n-many options for users to select, such that individuals can prioritize or weed through the masses. Especially in a sea of data on Ocean, it will be very important to help users effectively get to the most useful and insightful sets and tools to make sure that valuable time and resources are allocated to the most promising efforts. 

As mentioned in the initial Gitcoin grant, there are a variety of relevant metrics that should be considered in allocating resources/votes to various datasets and algorithm within the Ocean ecosystem.

Individual purchases from unique addresses is a first step in capturing how “popular” or in-demand a data set is, but is still something that is difficult to be Sybil resistant, as it would be relatively easy to coordinate multiple small purchases from connected accounts, as one address does not equal one real user.

Using other identity sources such as Twitter, Github authentication, etc. may help, but it is still possible for users to create multiple accounts.

Another approach would be to look at the repeat purchasing patterns of a user and with a “life-time staking value” as mentioned in the Gitcoin grant proposal, something that allows a user to signal for the value of an algo over a longer period of time is more useful information.

Thus, pure transaction volume in payments for a given algo is definitely the purest proof that it is valuable.

However, this would create a difficult incentive to increase the price of valuable algos, rather than allow users to have good algos at affordable prices; this is where a staking component is particularly helpful.

Ultimately, locking OCN tokens allows users to put their money where their mouth is, and really get some skin in the game in supporting and filtering the top algos. These funds are not “paid” and lost forever, but instead are locked in support of relevant algos that are undervalued. This allows the user to act a bit more aggressively in supporting valuable, well-priced algorithms, rather than overpriced ones.

We suggest a 50-50 weighting between transaction volume and staked value at the beginning, with this parameter open for adjustment after the first round.

Transaction volume’s 50% weighting would be calculated with itself  20% (10% overall) weight on lifetime volume, and the other 80% (40% overall) on volume within the last 14 days, to make sure that this data has a balance of new and old information on every algo’s volume.

It’s also important that a voting system like this is not overly complex, so it should not include two redundant scores that cover the same sentiments (for example, unique github voters and github stars, by which you need to be a unique github user to give a star - in this case, a star would be sufficient).

With regards to activity/frequency of commits, there needs to be a balance of “freshness” as well as “if it ain’t broke, don’t fix it”. Looking at recency of last commit can be easily gamed, as an update to a readme would be enough to trigger this. However, we do want a way for users to “refresh their algorithm or prove that they have recently been maintaining this algorithm.

With regards to staking, the earlier an individual stakes, the faster we can give feedback to other users saying that this algorithm is relevant. Thus, there should be a reward or power within the the duration of the round that rewards early voting within a round, such as to incentivize early action. Users should not be waiting to the very end of the round to see what has the best matching or highest power early.

Instead, we can create a formula in which at the start of a round, the first 10 votes within the round carry a 2x multiple on votes - this also incentivizes the early votes to be “large votes”, such that the multiple goes on a larger amount. 

Afterwards, we can use the simple quadratic formula, where subsequent votes increase marginal cost linearly. 

However, we would like to propose an additional parameter, which would be locktime, which adds a multiple to the base quadratic formula. 

To keep with the simplicity of the basic linear marginal cost increase, we should also reward in a simple manner users who are confident in the validity of the algorithm over a longer period of time. Thus, we give users the option to lock their funds for 1 week, 4 weeks, 9 weeks. The longer one votes, the larger the multiplier. We propose the weighting to increase by 1.25X and 1.5X, respectively, if a user decides to lock funds for the two longer-term signals. This allows for a user with less funds to make a larger impact on the vote if he is very confident in the legitimacy of an algo.

Finally, we want to make sure that votes are fresh, such that there can be a vote decay formula, in which a user’s vote needs to be refreshed within 6 weeks in order to have full efficacy. This is to ensure that voters have an incentive to revisit their past votes and make sure that their votes are constantly heard. We hope to build this via interface so users can signal their continued support of past votes. 

After this 6 week mark, their vote starts to decay a fixed 10% each week, such that after 16 weeks from initial vote, the vote becomes **stale. **

This will allow for votes from previous rounds to have an effect that is only limited to some recency bound, without completely disregarding past votes.  \


Finally, with regards to vote, we can allow for the score of one vote to carry over 20% weight into the next round of vote, such that algos with relevance in the previous round have a slight advantage as an incumbent, but not so as to stifle innovation and new competitors in the next rounds.

We finally allocate the number of github stars a set maintains as a 5% free weight against the 50% staked vote weight and 50% volume based weight, in which a team’s algo may be able to earn some votes purely from being a popular choice within the Github community. This however, limits the possible maximum that any fraudulent or malicious sybil attacks may have on the vote. In effect, this is a way to get GitHub users, a community that is valuable (in terms of developer attention time) and useful to the Ocean Protocol ecosystem, and starring good algorithms will help promote them in the activity feeds of Github Users. 

This 5% free weight may be in the future adjusted via governance vote/replaced by other relevant, easy to grab metrics that require some level of authentication in order to “vote” for free.
