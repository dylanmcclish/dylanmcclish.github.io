---
layout: post
title: "what reinforcement learning teaches us about decision-making"
date: 2026-07-22
---

something that has been on my mind a lot recently is how we optimally make decisions. i have been reading annie duke’s thinking in bets, which has emphasized looking at life through a probabilistic lens. it has helped me a lot in feeling empowered about how i navigate life through simply thinking of it as a game, where i understand the risks that i am taking. though, it is hard to maintain this perspective.

on this note, i have been learning about reinforcement learning recently for my research thesis at princeton. i find the concept of generalized policy iteration very representative of how we optimally learn and make decisions through life, in a similar vein to duke’s book. essentially, in reinforcement learning, we go through a dual process of evaluating a policy (way to make decisions in the environment), and then improving said policy.

in computationally evaluating the policy, we go through each state and calculate the long-run expected value of the action(s) that we would take in that state. however, this is a recursive problem as the long-run expected value of an action taken in a given state requires a long-run expected value of actions taken in the future states that we may transition to.

though, this is proven to converge to an accurate evaluation of the policy given enough iterations. then once we have these evaluations we can update the policy by comparing the value of the policy to values of alternative policies. these alternative policies typically are simply the value of taking another action in a given state, and then for all subsequent states just following the policy. it turns out, if this value is greater than the value that we originally found for the policy, then always taking this action in that state is more optimal. so, we update the policy accordingly. this updated policy is then re-evaluated and this process repeats. this is proven to converge to the optimal policy.

what i find fascinating is that we don’t actually have to fully evaluate the policy to converge to the optimal policy. we can simply do one iteration of the above computation — going through each state and calculating E.V of the policy in that state through using our previously-calculated E.V of the policy for all future states — to then update the policy. this is the difference between policy iteration (a complete computation of the policy evaluation) and value iteration (a single iteration of the policy evaluation).

in general, i think this says something about how we optimally navigate the human experience. we don’t need complete information. we don’t need to thoroughly understand exactly the process that we are using in order to improve it. all we need to do is to construct estimates, to evaluate it, even in some crude sense, using information about our existing process. then, we can use these estimates to update our process.

i struggle overarchingly with being a perfectionist. but, as i get older, i realize that not everything has to be perfect. in fact, everything should not be perfect. mathematically, we often can reach near-optimal results in a exponentially faster fashion if we cut corners, deliberately. this is not to say that we should just be cutting corners willy-nilly. but, if we can consciously make approximations about the long-run expected value of how we currently make decisions or navigate our environments, then we can leverage those to pivot.

i probably have no idea what i’m talking about,

dylan mcclish
