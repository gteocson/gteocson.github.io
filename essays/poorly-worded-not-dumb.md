---
layout: essay
type: essay
title: "Poorly Worded Doesn't Mean Dumb"
# All dates must be YYYY-MM-DD format!
date: 2015-09-08
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## You won't sound dumb (probably)

Now I don't want to discourage anybody from asking questions. I believe asking questions are important and even if the answer may be obvious in hindsight at least the experience will help you. However, I do believe asking questions is a skill that needs to be learned and practiced. In the software engineering field there is so much room for diversity. There are many different coding languages, environments, there could be issues with the hardware or bugs from other programs. Being able to ask good questions will allow you to find good answers and learn more.

```
Q: How can I pivot a dataframe?

The problem with existing questions and answers is that often the question is focused on a nuance that the OP has trouble generalizing in order to use a number of the existing good answers. However, none of the answers attempt to give a comprehensive explanation (because it's a daunting task)

Look a few examples from my Google Search

How to pivot a dataframe in Pandas?
Good question and answer. But the answer only answers the specific question with little explanation.
pandas pivot table to data frame
In this question, the OP is concerned with the output of the pivot. Namely how the columns look. OP wanted it to look like R. This isn't very helpful for pandas users.
pandas pivoting a dataframe, duplicate rows
Another decent question but the answer focuses on one method, namely pd.DataFrame.pivot
So whenever someone searches for pivot they get sporadic results that are likely not going to answer their specific question.

Question(s)
Why do I get ValueError: Index contains duplicate entries, cannot reshape

How do I pivot df such that the col values are columns, row values are the index, and mean of val0 are the values?

 col   col0   col1   col2   col3  col4
 row
 row0  0.77  0.605    NaN  0.860  0.65
 row2  0.13    NaN  0.395  0.500  0.25
 row3   NaN  0.310    NaN  0.545   NaN
 row4   NaN  0.100  0.395  0.760  0.24

```

The question actually has a lot more information then shown above and I highly encourage you to look at it [here](https://stackoverflow.com/questions/47152691/how-can-i-pivot-a-dataframe). The creator of the question includes code that they are testing as well as other questions relating. Now the only gripe I have with this is it might be too much. Yet there is a lot of good in it. The person has shown that they have down previous research and has done some experimentation.

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
