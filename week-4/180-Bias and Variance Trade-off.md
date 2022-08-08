## Bias and Variance in the real world

In dictionary terms:

**Bias:** Prejudice in favor of or against one thing, person, or group compared with another, usually in a way considered to be unfair.

**Variance:** The state or fact of disagreeing or quarreling.

In short, Bias represents how unfair something is toward others, and Variance represents how likely something changes with respect to others.

Confusing? Worry not. The following example will clarify all your doubts.

## Example

Let's assume you have called two weather examiners, Mr. Bishop and Mr. Varian, to test if it will rain or not.

Mr. Bishop loves rain a lot. And Mr. Varian is a bookworm. Let us talk about the conditions for rain.

* **It rains only when it's a little humid.**
* **It does not rain if it's windy, hot, or freezing.**

### Mr. Bishop representing Bias

You ask Mr. Bishop (Despite his training, he is too biased toward rain):

Me: Sir, it's extremely hot out here. Will it rain?

Mr. Bishop: Yup.

Me: Sir, it's a bit windy. Will it rain?

Mr. Bishop: Maybe not.

Me: Sir, it's freezing. Will it rain?

Mr. Bishop: Yes, of course.

Me: Sir, it's a little humid. Will it rain?

Mr. Bishop: Damn sure.

Did you notice that Mr. Bishop is highly Biased towards the chances of having rain? During the test, he is unable to predict most of them correctly.

This condition is called **under fitting**.

### Mr. Varian representing Variance

Now let us see your conversation with Mr. Varian (a bookworm who completely remembers the training he had):

Me: Sir, it's extremely hot out here. Will it rain?

Mr. Varian: Nope.

Me: Sir, it's a bit windy. Will it rain?

Mr. Varian: No way.

Me: Sir, it's freezing. Will it rain?

Mr. Varian: No way.

Me: Sir, it's a little humid. Will it rain?

Mr. Varian: Yes, it will.

Mr. Varian successfully predicted whether it would rain or not. But being a bookworm, Mr. Varian is unknown to the conditions not described in the book during training.

Now, we ask Mr. Varian :

Me: Sir, a giant who lost his candy, is sitting on the cloud. Will it rain?

Mr. Varian: Not sure. Since the answer is "No" to most of the conditions, there is a high possibility that it will not rain.

Now, although the decision of Mr. Varian varies perfectly with the input conditions, he cannot predict based on the new and unseen conditions (other general conditions apart from the given specific conditions while training).

This condition is called **overfitting.** And it offers **poor generalizability**.

## High Bias or High Variance?

Then what is better, high Bias (high generalizability) or high Variance (high accuracy on training data)?

Well, the answer is, "Best of both worlds". We neither need high Bias nor high Variance. We would want our algorithm to perform better on the training set and offer the best result on unseen data (the test set).

In general, **having high Bias reduces the algorithm's performance on the training set while having high Variance reduces performance on unseen data.**

This is known as the **Bias Variance Trade-off**.

### Reading Material

MUST READ

Understanding the Bias Variance Tradeoff:  https://towardsdatascience.com/understanding-the-bias-variance-tradeoff-165e6942b229

### Reference

https://medium.com/@viveksingh.heritage/an-intuitive-explanation-to-bias-variance-tradeoff-ec540fb13e12

### Slide Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1c_mkhl2ac9gapFwCQdn6tySCi09Ve8jCv8Z1BqbrPG8/edit?usp=sharing).