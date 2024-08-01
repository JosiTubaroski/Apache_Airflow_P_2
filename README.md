# Apache Airflow P 2

### The big leap strategy of Apache Airflow 2.0

In my opinion, Apache 20 was a game changer for Apache Airflow 

I can definitely say that you can go, you can put in Kubernetes or you can put it anywhere you want and you're going to be able to run at scale pretty easily.

You can scale out pretty much all the components. Right.

And because of this, I think we started to see shorter cycles, development cycles.

And another big thing, a big leap for Apache, airflow in my opinion, was brand breaking down or removing the packages from the Core Airflow code.

What are the major benefits that you've seen on this approach?

Because I know from now on, be much faster to realease and roll out new features and capabilities because of that huge transformation and code refactory that you guys did.

So one of the biggest motivation was so if the biggest motivation was so if you techinically think from development lifecycle, right, core has to be stable, the sheduler has to be stable.

But that also means that it's a lot more testing than probably the integration does. And if the Core goes wrong, it can have bad effect on your business.

But if integration goes wrong, you can just revert back to the last version So it's like, does it make sense to bundle them up in the same package?

This is when we were thinking of two daughters. So we said, what if we separate the operators and everything into something called providers and release it separately.

So the biggest benefit is like now Core can move along at its own pace, where integrations can move along at a very fast pace.

Because there was hesitancy for people or even frustrations, like, hey, I created a PR that was merged like four months ago.

We still don't have a release because, well, everything was tied the Apache Airflow Core repo and reduced a single artifact in one tech.

So we said, yeah, let's something about it. And that's when we separeted into logical groups of providers, logical groups of Integrations.

Google cloud provider can move at its own pace.

We can have different maintainers if you want.

Like Google has this managed service for Airflow. They could take a huge part into maintaining their own Google cloud provider.

And integration similar with AWS. I think that's the biggest benefit really scaled is faster as a user for you.

If something goes wrong, you can just revert to an older version. Upgrading provider should be very seamless because it does not impact code.

Whereas if you want to upgrade your Airflow just for an integration change, and if you have to migrate your database, that feels wrong.

It's like, why is this coupling?

So I think we just made it more natural, both from maintenance perspective, API maintenance, keeping up with new APIs for those integrations, and simpler management for Core.

Now, people who really work on Core scheduler and stuff like that can be separate people from people who work on integrations and review those.

So from even maintainability perspective it made a lot more sense and it is a lot more easier than if everything was club into a single thing, breaking down the pieces and micromanaging that it's way better.

And you can have specialist next page in each one of these areas contributing to them.

We have an extensive list of exciting new features after Tudor. 

We're not going to go for that because we have other exciting questions for you.

So I would like to take the most of your time here but I'm going to ask you to comment in two or three things pretty quickly.

What's your thoughts about the Task Force API which for me is a big lip and game changer.

Task API is definitely a game changer think it makes it easy for you think in terms

