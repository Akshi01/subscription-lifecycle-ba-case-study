## Problem Statement

Learnova is a subscription-based learning platform for professional courses. Currently, when the learners have to take a temporary break (e.g., due to exams, vacation, etc), they have to cancel their subscription and re-purchase to continue learning. Recent data shows a 70% drop-off after cancellation, and among returning learners, most show a gap of 1-2 months before re-purchasing. This results in significant revenue leakage, disrupted learning continuity and reduced learner retention.

---

## Business Objectives

- Reduce post-cancellation churn from **70% to 50% within 6 months**
- Improve overall learner retention by **15% – 20% within 12 months**
- Reduce the gap between cancellation and repurchase from **1–2 months to under 2 weeks**
- Increase Monthly Recurring Revenue (MRR) by **20% within 12 months**

---

## Proposed Solution

Learnova plans to introduce additional subscription features instead of a strict cancel-or-continue approach. The proposed features include:

- Pause Subscription: Learners can temporarily pause their subscription when they need without losing their progress
- Upgrade Subscription: Learners can move to a higher plan when they need advanced features.
- Downgrade Subscription: Learners can move to a lower plan when they need basic features.

These options will give learners more flexibility and control over their subscription, reducing the likelihood of full cancellation and helping maintaining learner continuity. 

---

## Stakeholders

The stakeholders identified are:

- Project Sponsor
- Project Manager
- Product Manager
- Business Analyst
- Development Team
- Testing Team
- Design Team
- Accounts Team
- Marketing Team
- Learnova learners

### Interest-Influence Matrix

Stakeholders were analyzed using an Interest–Influence matrix.

<img width="1023" height="796" alt="Screenshot (317)" src="https://github.com/user-attachments/assets/3ac715af-49fc-4028-8495-4829865c483b" />


---

## Requirement Gathering Approach

In order to understand the current challenges and define requirements for this initiative, the following methods were used:

- **Data analysis** to identify churn patterns and support data-backed decision making
- **Stakeholder Interviews** to understand their expectations, constraints and priorities
- **Existing process review** to identify the gaps in the current subscription workflow

The requirements were finalized after aligning business goals, user needs, and technical and financial feasibility.

---

## Key Requirements

### Business Requirements

- BR-01: The business needs to provide flexible alternatives to cancellation to reduce churn and improve revenue continuity.
- BR-02: The business needs to ensure learning continuity to improve learner retention

### Functional Requirements

- FR-01: The system should allow users to pause their subscription.
- FR-02: The system should allow users to upgrade their subscription plan.
- FR-03: The system should allow users to downgrade their subscription plan.
- FR-04: The system should retain learner progress during subscription changes.

### Non-Functional Requirements

- NFR-01: The system should allow users to pause their subscription within 5 seconds
- NFR-02: The system should reflect upgraded plan capabilities within 5 seconds.
- NFR-03: The system should reflect downgraded plan capabilities within 5 seconds.
- NFR-04: The system should process plan upgrade payments within 2 seconds.

### Business Rules

- BRR-01: The proposed features shall be applicable to the existing users as well as the new users.
- BRR-02: Learners shall be allowed to pause their subscription up to two times within a payment cycle
- BRR-03: Total duration of subscription pause per payment cycle shall not exceed 30 days
- BRR-04: Total duration of subscription pause across the subscription shall not exceed 100 days
- BRR-05: Learners shall be allowed to upgrade or downgrade their subscription up to two times each within a payment cycle
- BRR-06: Refund for the downgrades shall be processed in credits

---

## Scope

- Functionality to pause subscriptions
- Functionality to upgrade or downgrade subscriptions
- Retention of learner progress during plan change

## **Out of Scope**

- Mid-cycle subscription plan changes
- Refunds in the original payment source

---

## **Constraints**

- The initiative must be completed within 3 months to align with the upcoming peak season.
- The subscription related features must remain aligned with the current payment cycle structure
- The solution must be implemented in alignment with the current billing system, without introducing new billing functionalities.

---

## **Risks**

- Learners may use the pause subscription feature and still abandon the platform, resulting in limited improvement in churn metrics.
- Learners may overuse the downgrade option, which could negatively impact the Monthly Recurring Revenue (MRR)
- Introduction of new subscription functions may lead to an increase in number of customer support tickets

---

## User Stories

- As a learner, I want flexible subscription options so that I can choose a plan that matches my current needs
    
    **Acceptance Criteria**: Given I have an active subscription, When I go to the ‘Manage Subscription’ section, Then I should be able to pause, upgrade or downgrade my subscription.
    
- As a learner, I want to pause my subscription when needed, so that I don't pay when I am unable to learn
    
    **Acceptance Criteria:** Given I have an active subscription and didn't exceed the allowed pause limit, When I go to the ‘Manage Subscription’ section, Then I should be able to pause my subscription.
    
- As a learner, I want my learning progress to be saved after I resume the subscription, so that I can continue from where I left off
    
    **Acceptance Criteria**: Given I have paused my subscription, When I resume my plan, my previous progress should be visible 
    
    And I should be able to resume from where I left off
    
- As a learner, I want to downgrade my subscription so that I don't pay for the features I don't currently need.
    
    **Acceptance Criteria**: Given I have an active advanced subscription, When I go to the ‘Manage Subscription’ section, Then I should be able to downgrade my current plan And no longer have access to the features in the higher-tier plan.
    
- As a learner, I want to upgrade my subscription so that I can access additional features when required.
    
    **Acceptance Criteria**: Given I have an active basic subscription, When I go to the ‘Manage Subscription’ section, Then I should be able to upgrade my current plan and gain access to additional features in higher-tier plan
    

---

## As-Is / To-Be Flow

### As-Is Flow:

1. Learner has an active subscription 
2. Learner needs a temporary break 
3. Learner explores available options
4. Cancellation is the only option
5. Learner cancels their subscription 
6. Learner loses their progress and continuity 
7. Learner may never return 

### To-Be Flow:

1. Learner has an active subscription 
2. Learner needs a temporary break or a change in plan 
3. Learner explores available subscription options

**Path A - Pause**

1. Learner selects the pause subscription option
2. Learner’s progress remains intact during the pause period
3. Learner resumes the subscription when ready
4. Learner continues learning from where they left off

Path B - Upgrade/Downgrade

1. Learner selects an appropriate subscription option (upgrade or downgrade)
2. Learner’s plan is updated and feature access is adjusted accordingly
3. Learner’s progress remains intact after the subscription change
4. Learner continues learning with the modified plan

---

## Success Metrics

- **Feature adoption rate:** Usage rate of pause, upgrade, and downgrade options to measure learner adoption of the new subscription features.
- **Churn and retention rates:** To assess the impact of the new subscription features on learner behavior.
- **MRR change:** Changes in Monthly Recurring Revenue (MRR) to assess business impact.
- **Cancellation rate:** To track whether flexible options reduce full subscription cancellations.

---

## Assumptions

- Learners value flexibility in the subscription plans
- Learners are likely to return after pausing their subscription
- The system have sufficient capacity to store and retain learner's progress data
- The current billing system is equipped to support the proposed subscription changes
- Providing flexible subscription options will help reduce churn and cancellation rates

---

## Prioritization

- FR-01: The system should allow users to pause their subscription → Must Have
- FR-02: The system should allow users to upgrade their subscription plan. → Should Have
- FR-03: The system should allow users to downgrade their subscription plan. → Should Have
- FR-04: The system should retain learner progress during subscription changes. → Must Have

---
