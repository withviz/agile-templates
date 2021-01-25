# User Stories

**User stories** are a core component of the Agile framework, shifting the focus from software requirements to a user-centric description of desired capabilities. User stories are intentionally short and simple, focused on one particular feature written from the perspective of the user of a system rather than the system's developers.

They're different from traditional software system requirements in that they bring end users to the center of the conversation, adopting a more informal language to provide context for the developers of the system. A user story thus constitutes an **end goal**, **a desired functionality from the perspective of the user**, **not necessarily articulated in technical terms and agnostic to the engineering efforts that it entails**.

As a product owner or team lead, it is your (and your team's) job to refine user stories such that they constitute small, "atomic" units of work in an Agile framework such as scrum or kanban. For example, in scrum, user stories are added to sprints to be "burned down" over the duration of the sprint, in which case it is important that the user story is small enough to fit into a sprint. It is also important to establish a clear set of acceptance criteria, which often involves discussions with the end users. In this guide, you will learn how to refine user stories and acceptance criteria with the Agile framework.<sup>[1]</sup>

## Format

User stories are often expressed as **persona** + **need** + **purpose**. It is then typically written in a simple sentence that follows the structure:

`As a [type of user], I want [an action] so that [a benefit/a value].`

[1]: https://www.pluralsight.com/guides/refine-user-stories-and-acceptance-criteria-with-agile

## Capturing User Stories in Microsoft Teams

Whilst [AzureDevOps](https://azure.microsoft.com/en-gb/services/devops/) covers all of this and more, a simple way of collecting stories would be to use [Forms](https://forms.microsoft.com) and push the stories to a [Teams](https://teams.microsoft.com) list with [PowerAutomate](https://flow.microsoft.com)

### In Microsoft Forms

Create the form.

In the form description, explain to the user what you are doing and give an example of a response.

Create 1 question: "As a [type of user], I want [an action] so that [a benefit/a value]."

Save and copy the share url.

### In Teams

Go to the most appropriate channel and add `lists` and `PowerAutomate`.

Create a new list in a Teams Channel with the following fields

| User | User Story | Status | Priority | Acceptance Criteria |
| :--| :--| :--| :--| :--| :--|
|||||

### In PowerAutomate

Create a new flow with the following

![power automate](./assets/powerautomate.png)

Details of the flow

| Item | Details |
|:-- | :-- |
| When a new response is submitted | Choose your form |
| Get response details | `Form ID` is your form; `Response Id`  =  `Response Id`|
| Create Item | `Site Address` = your SharePoint site; `List name` = your new list; `User` = `Responder's email`; `User Story` = the question; `Status Value` = To Do; `Priority Value` = 3; `Acceptance Criteria` = keep blank |

Save.

Share the form with your target audience. A new user story will be added to the list whenever a new response is submitted.
