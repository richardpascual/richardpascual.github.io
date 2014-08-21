#Clawing Ourselves Down from a Stack of Monotony

I have been on Stack Overflow for some time now, and it is tiring to see the following algorithm develop on this site among users and answering responses:

        begin

          set so_id = my_name;
          get all_posts(type = unanswered, tags = topic_a, topic_b)

          loop
              get question;
              answer question;
              pop question stack;       -- sorry, couldn't resist a "stack" pun...
              collect points;

          end loop;
        end;


Now to make things slightly worse, take this and make it a sub-function of this:

        begin

           set answer_scope = daily;
           loop (over next ten years)
              execute question_farming(current_day);
              increment day;       
           end loop;
        end;


The questions that are littering our landscape are the typical newbie items that should be just compiled in a single 10-20 page FAQ... 

> instead, these _FAQ-shards_ are repeated randomly throughout the site by users who have 0 reputation and sometimes **don't even return a second time** to get their answer... so you can have a stellar answer to a noob question, but then it gets lost when people do the typical "sort by score"...

I am just as prone to this as the next answerer, but this should stop.  I have seen on other posts here on META an excellent starting point for a vision for this Stack Exchange themed expert site:

> WE are more than an expert site.  This ***IS A SITE FOR EXPERTS***.  There is a difference...

When ***I say "expert", that is not a skill-level or years-of-experience assessment...*** it is a statement of something deeper... the mindset of the professional (or hobbyist) involved. 



##Fielding "Grounders"

I don't mind answering things that have become trivial from my point of view, but let's NOT make this site a place where experts waste their time with monotonous, repetitive Q&A discussions or two line responses.  Don't answer the question... answer to the concepts involved.  In the past, most expert sites expect future researchers to dig deep into an obscure problem to see if the answer even applies to their own problem.

[@Gerrat](http://meta.stackoverflow.com/users/429982/gerrat), your perspective is insightful because it attempts to go at least one level deeper than a how-to/DIY style question.  Some follow-on explorations of my own:


1. What are you trying to accomplish with a "**unique** set of permutations"?  If you can't give away the specifics of your application, have the decency to abstract it into something else others can understand and follow if they want to learn the underlying concept:  BE CREATIVE.  I get annoyed with this A, B, C stuff.[1]  At least try exploring data-sets and test values to engage others... 

2. Why Python?  Could there be a better language or method for developing a solution?  This begs the question, but this is where a `STACK OVERFLOW "EXPERT"` will shine.  The experts in this realm are inquisitive enough to reconsider and assess even things that are already assumed unchangeable.

3. Now that I have seen how it works from end to end, how can I make this hot-rod SCREAM with performance?  As with any gear-head (hey, even developers have their own variation!), the fun part should be to figure out creative ways of squeezing awesome throughput into the design.

4. Discussions for other uses, applications, predictions/projections for the future... opinions backed with examples, and CROSS-POSTING[2] links to other Stack Overflow discussions from past and present...


##Some Examples of Follow-on Explanations

Here is an example from [a recent post](http://stackoverflow.com/questions/25389417/trying-to-create-an-apex-link-column-that-queries-a-report) I made in response to a very general design concept in Oracle APEX.  I got zero reputation from the owner of the OP, but I don't mind.  


![An Example of a "Fresh" Test Data Schema][3]


(I also don't mind tackling questions that were misunderstood and buried under lots of negative site-karma... if their topic has some utility.)[4]  


> ***Ladies and gentlemen, we have seen the future, and it's a scattered landscape of "Search Engine" gamers... Q&A cookie-cutter forums, blogs and websites... you know the kind: 80% ad-space and 20% content scraped from old online pdfs from the major software houses... or worse, scraped from even OLDER forums with poor SEO. Stack is still far from this, but let's make a stronger effort at avoiding looking like them even more.***



##Call to Action and Some Good News

An Obsevation:  Something cool is happening these days.  Try searching anything technical in your field... something general or easy.  I have noticed at least in my arena (Oracle, database, etc.) SO originated posts are top ranking search results... consistently.  It may not be from cross-linking or advertising and marketing... I didn't see a SuperBowl Ad, so it can't be that... My intuition tells me it's because SO maintains a good proportion of QUALITY content, spot-on answers and community managed BS meters... that's really a great reputation to have.

You can answer any and all questions across the board, nobody is blocking you. Experts should however, bring _something else_ to the table that makes a plain answer (the "easy-A") an "**expert** answer" (the "A+" on top).  



***So what will it be, Stack Experts?***



[1] For database developers, scott/tiger is almost two decades old!  I get the "recent" Peoplesoft acquisition, but not every problem in the database world looks like an HR issue!

[2] Why should cross-posting be an issue? It reinforces the overall search scope of a problem and other problems that are related by many different overlapping concepts.
             
[4] The OP wanted SQL code and a sample report output for a non-existent data set... grounding sample data to "real"-world patterns makes it faster to absorb the concepts at hand.


  [3]: http://i.stack.imgur.com/m7U5H.jpg
