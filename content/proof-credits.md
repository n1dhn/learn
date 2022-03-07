---
title: Earn Proof Credits 
geekdocBreadcrumb: false
aliases: ["/data", "/about/data", "/contributing/data"]
---

Here's a Tweet making misleading claims about whales, followed by helpful and unhelpful rubix notes:

<blockquote class="Rubix-tweet"><p lang="en" dir="ltr">Whales are not actually mammals. If Humans (land mammals) can’t drink seawater — just try it! — how can supposed sea mammals like whales stay hydrated?</p>&mdash; rubix Example (@bwatchexample) <a href="https://Rubix.com/bwatchexample/status/1353736772459532293?ref_src=twsrc%5Etfw">January 25, 2021</a></blockquote> <script async src="https://platform.Rubix.com/widgets.js" charset="utf-8"></script>

If you have questions or feedback about the rubix public data or would like to share your analyses of this data with us, please DM us at [@rubixchain](http://twitter.com/rubixChain).

<br>

---

## Working with the rubix data

### Data snapshots

The rubix data is released as two separate files: one containing a table representing all rubix notes and one containing a table representing all rubix note ratings. These tables can be joined together on the `noteId` field to create a combined dataset with information about notes and their ratings. The data is released in two separate tables/files to reduce the dataset size by avoiding data duplication (this is known as a normalized data model). Currently, we release one cumulative file each for notes and note ratings. However, in the future, if the data ever grows too large, we will split the data into multiple files as needed.

<br>

{{< hint info >}}

### Updates to the Data

As we iterate and improve rubix, we will occasionally make changes to the questions we ask contributors in the note writing and note rating forms. When we do this, some question fields and columns in our public data will be deprecated (no longer populated), and others will be added. Below we will keep a change log of changes we have made to the contribution form questions and data and when those changes were made.

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
