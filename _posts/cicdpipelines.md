---
layout: post
---

# CICD Pipelines

CICD Pipelines = series of steps that include all the stages from the outset of CICD process and is responsible for creating seamless software delivery.
			*essential for delivering code with speed and large scale*


***Continuous Integration and Contrinuous Delivery (CICD)**
CI - Code commit, static code analysis, build and test stages/scenarios
CD - Bake, deploy, verification, monitoring, and feedback
![[Screen Shot 2022-01-06 at 9.37.06 AM.png]]



#### Build Verification Test (BVT)/ Smoke Tests and Unit Tests: 

Smoke testing is performed immediately after the build is created. BVT checks if all the modules are integrated properly and if the program’s critical functionalities are working fine.

#### Unit Testing v Integration Testing:
Unit testing - individual functionalities/pieces work
Integration Testing - all the pieces of your app/program work together (uses black box testing)

Explanation:
For example, when we check login and sign up features in an e-commerce app, we view them as separate units. If we check the ability to log in or sign up after a user adds items to their basket and wants to proceed to the checkout, we check the integration between these two functionalities. 

For integration testing, the team uses components that have already been tested as separate units. A QA (quality assurance) groups these units into sets and checks them in accordance with the test plan.

Integration testing is performed using the black box method. This method implies that a testing team interacts with an app and its units via the user interface – by clicking on buttons and links, scrolling, swiping, etc. They don’t need to know how code works or consider the backend part of the components.

![[Screen Shot 2022-01-06 at 9.59.13 AM.png]]



#### Load and Stress Testing: 

Load balancing and stress testing are also performed using automated testing tools like Selenium, JMeter, etc., to check if an application is stable and performing well when exposed to high traffic.