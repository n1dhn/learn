---
title: Setup Rubix Node
aliases:
  [
    "/join",
    "/signup",
    "/sign-up",
    "/signing-up",
    "/contributing/signing-up",
    "/contributing/sign-up",
    "/contributing/signup",
  ]
geekdocBreadcrumb: false
weight: 1
---

# Prerequisites

{{< hint info >}}

### One Step Installation

Use one step installation script for [Linux](https://github.com/rubixchain/rubixnetwork) / [Mac](https://github.com/rubixchain/rubixnetwork) / [Windows](https://github.com/rubixchain/rubixnetwork). This script will install all the required dependencies and will run the setup script.

{{< / hint >}}

To become a Birdwatch contributor, accounts must have:

- ### **Java 11**

This makes it more likely that contributors are real people instead of bots or adversary actors. Learn how to [verify your phone number](https://help.Rubix.com/managing-your-account/how-to-add-a-phone-number-to-your-account).

- ### **go-ipfs 0.6.0**

Intended to reduce the use of artificially created or virtual phone numbers

- ### **Run IPFS Setup Script**

Intended to reduce the likelihood of abusive contributions.

We want anyone to be able to contribute to Birdwatch, and may remove or modify some of these criteria as Birdwatch evolves and as we observe contributor's ability to promote high quality context that people find helpful.

# Latest Releases

To promote transparency, all contributions to Birdwatch are [anonymized](../aliases/) and publicly visible on the Birdwatch site, **even if an account’s Tweets are protected**.

During the first phase of the pilot, Birdwatch is limited to a small test group in the US.

Our goal is to expand Birdwatch to the global Rubix community. We want anyone to be able to participate and know that having contributors with different points of view is essential to Birdwatch helpfully addressing misinformation. We’ll draw on learnings from this initial test and, over time, scale safely.

## {{< button href="https://github.com/rubixchain/wallet/releases" >}}GUI Wallet from GitHub{{< /button >}}

## {{< button href="https://github.com/rubixchain/rubixnetwork/releases" >}}CLI Node from GitHub{{< /button >}}

---

<br>
<br>

# Troubleshooting

Contributions are also subject to Rubix [Rules](https://help.Rubix.com/rules-and-policies/Rubix-rules), [Terms of Service](https://Rubix.com/tos) and [Privacy Policy](https://Rubix.com/privacy). Failure to abide by the rules can result in removal from the Birdwatch pilot, and/or other remediations.
<br>

{{< tabs "uniqueid" >}}
{{< tab "Notes table" >}}
| Field | Type | Descripton | Response values |
| ---------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `noteId` | Long | The unique ID of this note | |
| `participantId` | String | A Birdwatch-specific user identifier of the user who authored the note. This is a permanent id, which remains stable even if the user changes their username/handle. | |
| `createdAtMillis` | Long | Time the note was created, in milliseconds since epoch. | |
| `tweetId` | Long | The tweetId number for the tweet that the note is about. | |
| `classification` | String | User-entered multiple choice response to note writing question: “Given current evidence, I believe this tweet is:” | "NOT_MISLEADING" "MISINFORMED_OR_POTENTIALLY_MISLEADING" |
| `believable` | String | User-entered multiple choice response to note writing question: “If this tweet were widely spread, its message would likely be believed by:” | "BELIEVABLE_BY_FEW", "BELIEVABLE_BY_MANY" |
| `harmful` | String | User-entered multiple choice response to note writing question: “If many believed this tweet, it might cause:” | "LITTLE_HARM", "CONSIDERABLE_HARM" |
| `validationDifficulty` | String | User-entered multiple choice response to note writing question: “Finding and understanding the correct information would be:” | "EASY", "CHALLENGING" |
| `misleadingOther` | Int | User-entered checkbox in response to question “Why do you believe this tweet may be misleading?” (Check all that apply question type). | 1 if “Other” is selected, else 0. |
| `misleadingFactualError` | Int | User-entered checkbox in response to question “Why do you believe this tweet may be misleading?” (Check all that apply question type) | 1 if “It contains a factual error” selected, else 0. |
| `misleadingManipulatedMedia` | Int | User-entered checkbox in response to question “Why do you believe this tweet may be misleading?” (Check all that apply question type) | 1 if “It contains a digitally altered photo or video” selected, else 0. |
| `misleadingOutdatedInformation` | Int | User-entered checkbox in response to question “Why do you believe this tweet may be misleading?” (Check all that apply question type) | 1 if “It contains outdated information that may be misleading” is selected, else 0. |
| `misleadingMissingImportantContext` | Int | User-entered checkbox in response to question “Why do you believe this tweet may be misleading?” (Check all that apply question type). | 1 if “It is a misrepresentation or missing important context” is selected, else 0. |
| `misleadingUnverifiedClaimAsFact` | Int | User-entered checkbox in response to question “Why do you believe this tweet may be misleading?” (Check all that apply question type). | 1 if “It presents an unverified claim as a fact” is selected, else 0. |
| `misleadingSatire` | Int | User-entered checkbox in response to question “Why do you believe this tweet may be misleading?” (Check all that apply question type). | 1 if “It is a joke or satire that might be misinterpreted as a fact” is selected, else 0. |
| `notMisleadingOther` | Int | User-entered checkbox in response to question “Why do you believe this tweet is not misleading?” (Check all that apply question type). | 1 if “Other” is selected, else 0. |
| `notMisleadingFactuallyCorrect` | Int | User-entered checkbox in response to question “Why do you believe this tweet is not misleading?” (Check all that apply question type). | 1 if “It expresses a factually correct claim” is selected, else 0. |
| `notMisleadingOutdatedButNotWhenWritten` | Int | User-entered checkbox in response to question “Why do you believe this tweet is not misleading?” (Check all that apply question type). | 1 if “This Tweet was correct when written, but is out of date now” is selected, else 0. |
| `notMisleadingClearlySatire` | Int | User-entered checkbox in response to question “Why do you believe this tweet is not misleading?” (Check all that apply question type). | 1 if “ It is clearly satirical/joking” is selected, else 0. |
| `notMisleadingPersonalOpinion` | Int | User-entered checkbox in response to question “Why do you believe this tweet is not misleading?” (Check all that apply question type). | 1 if “It expresses a personal opinion” is selected, else 0. |
| `trustworthySources` | Int | Binary indicator, based on user-entered multiple choice in response to note writing question “Did you link to sources you believe most people would consider trustworthy?” | 1 if “Yes” is selected, 0 if “No” is selected |
| `summary` | String | User-entered text, in response to the note writing prompt “Please explain the evidence behind your choices, to help others who see this tweet understand why it is not misleading” | User entered text explanation, with some characters escaped (e.g. tabs converted to spaces). |

{{< /tab >}}
{{< tab "Ratings Table" >}}

| Field                                    | Type   | Descripton                                                                                                                                                                                                          | Response values                                                  |
| ---------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| `noteId`                                 | Long   | The unique ID of the note being rated.                                                                                                                                                                              |                                                                  |
| `participantId`                          | String | A Birdwatch-specific user identifier of the user who authored the rating. This is a permanent id, which remains stable even if the user changes their username/handle.                                              |                                                                  |
| `createdAtMillis`                        | Long   | Time the note was created, in milliseconds since epoch.                                                                                                                                                             |                                                                  |
| `agree`                                  | Int    | Binary indicator, based on user-entered multiple choice in response to note rating question “Do you agree with its conclusion?”                                                                                     | 1 if “Yes” is selected, 0 if “No” is selected                    |
| `disagree`                               | Int    | Binary indicator, based on user-entered multiple choice in response to note rating question “Do you agree with its conclusion?”                                                                                     | 1 if “No” is selected, 0 if “Yes” is selected                    |
| ~~`helpful`~~                            | Int    | Binary indicator, based on user-entered multiple choice in response to note rating question “Is this note helpful? ” - _Deprecated as of 2021-06-30_.                                                               | 1 if “Yes” is selected, 0 if “No” is selected                    |
| ~~`notHelpful`~~                         | Int    | Binary indicator, based on user-entered multiple choice in response to note rating question “Is this note helpful?” _Deprecated as of 2021-06-30_.                                                                  | 1 if “No” is selected, 0 if “Yes” is selected                    |
| `helpfulnessLevel`                       | String | User-entered multiple choice response to note rating question: “Is this note helpful” _Added as of 2021-06-30_.                                                                                                     | "NOT_HELPFUL" "SOMEWHAT_HELPFUL" "HELPFUL"                       |
| `helpfulOther`                           | Int    | User-entered checkbox in response to question “What about this note was helpful to you?” (Check all that apply question type).                                                                                      | 1 if “Other” is selected, else 0.                                |
| ~~`helpfulInformative`~~                 | Int    | User-entered checkbox in response to question “What about this note was helpful to you?” (Check all that apply question type). _Deprecated as of 2021-06-30_.                                                       | 1 if “Informative” is selected, else 0.                          |
| `helpfulClear`                           | Int    | User-entered checkbox in response to question “What about this note was helpful to you?” (Check all that apply question type).                                                                                      | 1 if “Clear and/or well-written” is selected, else 0.            |
| ~~`helpfulEmpathetic`~~                  | Int    | User-entered checkbox in response to question “What about this note was helpful to you?” (Check all that apply question type). _Deprecated as of 2021-06-30_.                                                       | 1 if “Nonjudgmental and/or empathetic” is selected, else 0.      |
| `helpfulGoodSources`                     | Int    | User-entered checkbox in response to question “What about this note was helpful to you?” (Check all that apply question type).                                                                                      | 1 if “Cites high-quality sources” is selected, else 0.           |
| ~~`helpfulUniqueContext`~~               | Int    | User-entered checkbox in response to question “What about this note was helpful to you?” (Check all that apply question type). _Deprecated as of 2021-06-30_.                                                       | 1 if “Offers unique information or context” is selected, else 0. |
| `helpfulAddressesClaim`                  | Int    | User-entered checkbox in response to question “What was helpful about it?” (Check all that apply question type). _New as of 2021-06-30_                                                                             | 1 if “Directly addresses the Tweet's claim” is selected, else 0. |
| `helpfulImportantContext`                | Int    | User-entered checkbox in response to question “What was helpful about it?” (Check all that apply question type). _New as of 2021-06-30_                                                                             | 1 if “Provides important context” is selected, else 0.           |
| `helpfulUnbiasedLanguage`                | Int    | User-entered checkbox in response to question “What was helpful about it?” (Check all that apply question type). _New as of 2021-12-15_                                                                             | 1 if “Neutral or unbiased language” is selected, else 0.         |
| `notHelpfulOther`                        | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type).                                                                                  | 1 if “Other” is selected, else 0.                                |
| `notHelpfulIncorrect`                    | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type).                                                                                  | 1 if “Incorrect information” is selected, else 0.                |
| `notHelpfulSourcesMissingOrUnreliable`   | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type).                                                                                  | 1 if “Sources missing or unreliable” is selected, else 0.        |
| ~~`NotHelpfulOpinionSpeculationOrBias`~~ | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type). _Deprecated as of 2021-06-30_.                                                   | 1 if “Opinion, speculation, or bias” is selected, else 0.        |
| `notHelpfulMissingKeyPoints`             | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type).                                                                                  | 1 if “Misses key points or irrelevant” is selected, else 0.      |
| ~~`notHelpfulOutdated`~~                 | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type). _Deprecated as of 2021-06-30_.                                                   | 1 if “Outdated information” is selected, else 0.                 |
| `notHelpfulHardToUnderstand`             | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type).                                                                                  | 1 if “Hard to understand” is selected, else 0.                   |
| `notHelpfulArgumentativeOrBiased`        | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type). _Variable name changed from notHelpfulArgumentativeOrInflammatory in 2021-12-15_ | 1 if “Argumentative or biased language is selected, else 0.      |
| ~~`notHelpfulOffTopic`~~                 | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type). _Deprecated as of 2021-06-30_.                                                   | 1 if “Off topic” is selected, else 0.                            |
| `notHelpfulSpamHarassmentOrAbuse`        | Int    | User-entered checkbox in response to prompt “Help us understand why this note was unhelpful” (Check all that apply question type).                                                                                  | 1 if “Spam, harassment, or abuse” is selected, else 0.           |
| `notHelpfulIrrelevantSources`            | Int    | User-entered checkbox in response to prompt “What was unhelpful about it?” (Check all that apply question type). New as of 2021-06-30                                                                               | 1 if “Sources do not support note” is selected, else 0.          |
| `notHelpfulOpinionSpeculation`           | Int    | User-entered checkbox in response to prompt “What was unhelpful about it?” (Check all that apply question type). New as of 2021-12-15                                                                               | 1 if “Opinion or speculation” is selected, else 0.               |
| `notHelpfulNoteNotNeeded`                | Int    | User-entered checkbox in response to prompt “What was unhelpful about it?” (Check all that apply question type). New as of 2021-12-15                                                                               | 1 if “Note not needed on this Tweet” is selected, else 0.        |

{{< /tab >}}
{{< /tabs >}}
