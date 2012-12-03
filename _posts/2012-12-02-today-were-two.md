---
title: Today We&apos;re Two
author:
  name: Paddy Foran
  slug: paddy
categories:
  - posts
tags:
  - "author/paddy"
layout: post
---
Two years ago today, New York State said &quot;[Paddy](/team/paddy) and [Tino](/team/tino) want to start a company? What could possibly go wrong?&quot; and granted our little company status as a limited liability corporation in the state of New York.

<!-- break -->

## Growing Up Is Hard

Last year, we wrote [a blog post](/blog/losing-neverland-year-in-review) celebrating our birthday, too. In that post, we talked about a lot of things, but there was one central theme: we were going to start asking people to pay us to use our [most successful product](/2cloud).

This time around, we have another theme: why a year has passed and we&apos;re still not charging people for that product.

We&apos;ve grown a lot as a company and as people in the last year. Paddy is no longer a student, and upon entering the Real World, he discovered that you actually need money to live. Weird. This led to him getting a full-time job, working for a cloud computing startup. He loves it, but it takes up much more of his time than school did. Tino finished up his Master&apos;s in Business Administration, so he&apos;s become a much more skilled leader of the business. He, however, has also entered the Real World, which limits the time he can spend trying to maneuver our team into productivity and our finances into profitability.

To combat this Real World dilemma, we [brought Dylan onto the team](/blog/prettymaker-in-chief) on a temporary basis, trying to make up for Paddy&apos;s lost productivity. And that worked, for a very brief amount of time. Then Paddy had the brilliant idea of getting Dylan hired at the same startup he works at, and suddenly Dylan is strapped for time, too.

## Saying Goodbye To An Old Friend

We also made the decision to move off of App Engine. We loved App Engine. It was great. The people behind the service are amazing, the service fills a great niche, and the stability was amazing. But as we switch over to a paid model, we needed more control over the user experience in a few areas. A few features (even ones we helped shape) were not suited particularly well to our use cases. As the product grew in scope and complexity, it became clear that we were bumping up against the limits of App Engine.

In the last year, we&apos;ve been busily rewriting the application in [Go](http://www.golang.org), our new programming language of choice. We&apos;ve been learning about self-hosting. We&apos;ve been comparing hosts, weighing trade-offs, and attempting to prepare ourselves for our unique needs. In the process of doing this, we&apos;ve learned how much App Engine did for us that we never even thought about. 99.99% uptime. Load balancing. Distributed realtime functionality. Data storage with backups. All of these things are hard to do right, and we&apos;ve been experimenting and learning as we try to get them right.

A year ago, we published a private beta of Bessie, our newest version of 2cloud. We had a web interface working, and we wanted to gauge how we were doing in our efforts to replace App Engine. We learned pretty quickly that some of the things we were doing worked really well, but some were really bad ideas. We scrapped it and started from the beginning again.

At this point, we&apos;ve written and rewritten our server component at least three or four times. As we learn more about our needs and more about maintaining software and more about different database technologies and more about scalability, we rewrite our software to match it. We need to get this right from day one, because first impressions are important. More importantly, because taking your money is something we take very seriously. If we&apos;re going to ask you for money, we&apos;re going to be damn sure that the service we&apos;re providing is worth that money and is stable enough.

## Looking Ahead

This last year has been rough on us as a company. We struggled to stick together and keep our products under development, even though we released no updates or fixes to our flagship product in the last year. We struggled to keep our spirits up as we got bug reports for things we had no intention of fixing, as they would be replaced by superior software soon. We care deeply about the experience we offer to our users, and it bothers us when people get a bad experience. Our donations have trickled to almost non-existent levels, and the project has more or less been subsidised by our wallets for the last year. That&apos;s only to be expected; people shouldn&apos;t be paying for software that isn&apos;t being actively developed.

In the next 365 days, we have established a few goals:

* Release the latest and greatest update to 2cloud
* Become profitable. That means not only gaining enough users who pay us monthly to cover our monthly costs, but actually recouping the development costs from the last year and the deficit 2cloud&apos;s servers have accumulated over the years of their operation. It would mean when you look at the money we&apos;ve made over the lifetime of the service and the money we&apos;ve spent over the lifetime of the service, the money we&apos;ve made would be the bigger number.
* Establish a new balance. All our employees are working for other companies at this point, and Bessie requires so much work and concentration, it&apos;s hard to establish a good balance between working on our Second Bit projects and the rest of our lives. We&apos;d like to be putting in a consistent level of work on our projects, rather than huge chunks every now and then. We&apos;d like to be slowly iterating on these projects, so every week or two, users are getting a better experience.
* Share solutions to the problems we&apos;re solving. [Pastry](/blog/introducing-pastry) (now [Wendy](/blog/pastry-is-now-wendy)) was the most popular item on Hacker News the day it was released, so there&apos;s clearly a demand for more information about how to build the scalable, realtime systems that we&apos;re struggling with. We&apos;d like to, as the year progresses and we gain confidence in the technologies we&apos;re using, share those technologies and strategies with you.

We really appreciate all the support we&apos;ve received over the last two years. We hope you&apos;ll all stick with us for the future; it&apos;s going to be an adventure, and we wouldn&apos;t miss it for the world.