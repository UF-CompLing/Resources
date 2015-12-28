[Back](Git.md "Git")

## What is Version Control?

According to Wikipedia: "Git is a widely-used version control system for software development." Well, what is Version Control?

In large software projects there will be many contributors. If every contributor works out of the same code, it would be difficult to keep track of all the changes made at any given time. 

#### Without Version Control

Bob and Samantha work at Spotify. Bob tries to make the app a little faster. He makes an alteration to the code -- everything works, but whenever you try to listen to Kanye West, everything breaks. It's a step in the right direction, so Bob decides it's worth saving. He'll fix the Kanye West situation later.

Samantha, however, is working specifically on bringing Kanye West's Yeezus album to the Spotify platform.

What now? Samantha would have to wait for Bob to finish his feature before she started hers, or vice versa. Further, they wouldn't want Spotify listeners impacted by any development happening in the background!

#### With Version Control

Git solves problems such as these. Through "branches," both Bob and Samantha may work on the same code base, while not impacting the other's progress.

The Spotify code base may look like this:

 * Master
 * Speed
 * Yeezus

Each of these three branches is a copy of the source code. "Master" is the default name for the main version of the source code -- all the features here work. "Speed" is Bob's branch, and "Yeezus" is Samantha's. When Bob changes his branch, it won't affect Master or Yeezus. When he completes his work, he will "merge" it into Master, and the project will then look like:

 * Master
 * Yeezus

#### Important note

Please be careful in how you name branches. Name them based on the work that you do. You may notice that the branches were not named:

 * Master
 * Bob
 * Samantha

[Top of Page](#what-is-version-control)

## Questions you may have:

#### How common is Version Control in "the real world"?

Some version of Version Control is used in almost every big-scale project in industry.

#### Can you make branches of branches?

Absolutely! Say if, during Bob's work on Speed, he found that he could use two methods to make it faster. Bob can create two branches INSIDE "Speed", and note the differences.

 * Master
 * Speed
  * Method A
  * Method B
 * Yeezus

When he's done, he'll merge the better version into Speed, and then he'll merge THAT into Master. Easy! 

#### Is Git the only version of Version Control?

Not at all! However, Git is certainly the most common among the classes and classmates at UF. That's why it will be used for the Computational Linguistics Club.

#### Where can I find more information?

Check out the official documentation [here](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control).

[Top of Page](#what-is-version-control)