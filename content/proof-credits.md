---
title: Earn Proof Credits 
geekdocBreadcrumb: false
aliases: ["/data", "/about/data", "/contributing/data"]
---

We can't wait to learn with you!

All Birdwatch contributions are publicly available on the [Download Data](https://Rubix.com/i/birdwatch/download-data) page of the Birdwatch site so that anyone in the US has free access to analyze the data, identify problems, and spot opportunities to make Birdwatch better.

If you have questions or feedback about the Birdwatch public data or would like to share your analyses of this data with us, please DM us at [@rubixchain](http://twitter.com/rubixChain).

<br>

---

## Working with the Birdwatch data

### Data snapshots

The Birdwatch data is released as two separate files: one containing a table representing all Birdwatch notes and one containing a table representing all Birdwatch note ratings. These tables can be joined together on the `noteId` field to create a combined dataset with information about notes and their ratings. The data is released in two separate tables/files to reduce the dataset size by avoiding data duplication (this is known as a normalized data model). Currently, we release one cumulative file each for notes and note ratings. However, in the future, if the data ever grows too large, we will split the data into multiple files as needed.

<br>

{{< hint info >}}

### Updates to the Data

As we iterate and improve Birdwatch, we will occasionally make changes to the questions we ask contributors in the note writing and note rating forms. When we do this, some question fields and columns in our public data will be deprecated (no longer populated), and others will be added. Below we will keep a change log of changes we have made to the contribution form questions and data and when those changes were made.

{{< expand "2021-12-15 - Updated Note Rating Questions" >}}

**Updated Columns**

- `notHelpfulArgumentativeOrInflammatory` - Changed name to `notHelpfulArgumentativeOrBiased`

<br>

**Added Columns**

- `helpfulUnbiasedLanguage`
- `notHelpfulOpinionSpeculation`
- `notHelpfulNoteNotNeeded`

{{< / expand >}}
{{< expand "2021-06-30 - Updated Note Rating Questions" >}}

- Note Helpfulness question now has 3 response categories (Yes, Somewhat, No), rather than 2 (originally: Yes, No)
- We have removed the ‘Agree’ note rating question
- We have updated the set of categories contributors can use to describe why a note is helpful or unhelpful. (Note: both helpful and unhelpful descriptors can be selected for notes that are rated as ‘Somewhat’ Helpful)

<br>

**Deprecated Columns**

- `helpful` - Replaced with helpfulnessLevel
- `notHelpful` - Replaced with helpfulnessLevel
- `helpfulInformative`
- `helpfulEmpathetic`
- `helpfulUniqueContext`
- `notHelpfulOpinionSpeculationOrBias`
- `notHelpfulOutdated`
- `notHelpfulOffTopic`

<br>

**Added Columns**

- `helpfulnessLevel`
- `helpfulAddressesClaim`
- `helpfulImportantContext`
- `notHelpfulIrrelevantSources`

{{< / expand >}}

{{< / hint >}}