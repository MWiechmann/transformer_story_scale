# Table of Contents
- [Summary](#summary)
- [Motivation](#motivation)
- [Current Story Quality Measures](#current-story-quality-measures)
- [How Do You Measure Opinions, Anyway?](#how-do-you-measure-opinions-anyway)
- [Enter The AI Story Scale](#enter-the-ai-story-scale)
- [How To Cite The AISS](#how-to-cite-the-aiss)
- [FAQ](#faq)

# Summary
Research on the evaluation of AI-generated stories has yet to adopt a psychometrically validated scale for human evaluations. This poses a serious threat to the validity and reliability of research findings, as existing measures may not accurately capture the intended concepts or may not capture them reliably enough for results to be meaningful. The AI Story Scale (AISS) addresses this gap by providing a reliable and valid rating scale that draws on empirical research and best psychometric practices, enabling researchers and practitioners to evaluate the quality and nature of AI-generated stories with confidence.

# Motivation
Large-scale language models (LLMs) are awesome! The rapid advances of this technology in the last few years can only be described as truly breathtaking ([Min et al., 2021](https://arxiv.org/pdf/2111.01243.pdf); [Tang, Guerin, Li & Lin, 2022](https://arxiv.org/pdf/2203.03047.pdf)). As of time of writing (June 2023), tools like ChatGPT, GPT-4, and other emerging models continue to make headlines and capture the public imagination (e.g. [Bubeck et al., 2023](https://arxiv.org/abs/2303.12712), [Lee, Bubeck & Petro, 2023](https://www.nejm.org/doi/full/10.1056/NEJMsr2214184), [OpenAI, 2023](https://arxiv.org/abs/2303.08774)). These models are capable of remarkable feats, demonstrating impressive proficiency for tasks as complex and multi-faceted as storytelling ([Alhussain & Azmi, 2021](https://www.researchgate.net/profile/Aqil-Azmi/publication/351858590_Automatic_Story_Generation_A_Survey_of_Approaches/links/60afe2e0299bf13438efd3bc/Automatic-Story-Generation-A-Survey-of-Approaches.pdf); [Xie, Cohn & Lau, 2023](https://arxiv.org/abs/2301.09790)).

In fact, AI-generated storytelling is being adopted more and more across various industries. In the entertainment industry, AI is being used [for scriptwriting and storytelling](https://www.hollywoodreporter.com/business/digital/ai-storytelling-1235504180/). In the writing and authorship sector, AI story generators are becoming popular tools for writers, offering innovative ways to [overcome writer's block and find inspiration for their work](https://www.unite.ai/best-ai-story-generators/).
 
However, as impressive as the existing implementations are, the evaluation practices for generated text have been identified as flawed, with studies often not satisfying even basic requirements for sound empirical science ([Gehrmann, Clark, & Sellam, 2023](https://doi.org/10.1613/jair.1.13715)). This is an urgent issue; particularly as neural generation models have improved to the point where their outputs can often no longer be distinguished based on the surface-level features that older metrics rely on. Even measures that attempt to delve deeper, such as human evaluations, suffer from serious shortcomings. One of the most critical of these is one that is typically overlooked in research on large language models and AI more generally: the lack of psychometric validation.

Psychometric validation is essential to ensure that an instrument measures anything meaningful at all, and that it does so with precision. This lack of validation is a pressing threat to the validity of research in this field. It is this issue that the AI Story Scale (AISS) aims to address. The AISS provides a solid foundation for measuring the quality and nature of AI-generated stories, offering a solution to the shortcomings of current measures for human story evaluation. By providing a reliable and validated tool for evaluating AI-generated stories, the AISS can help researchers and practitioners better understand the capabilities and limitations of different models and generation settings.

I suspect that many readers at this point might be thinking, "Psychometric what now?". If that is you, you might be skeptical about the need for yet another way of evaluating AI generated text. I get it.

However, bear with me - I will try to explain why this is so important and how the AI Story Scale could make a significant difference in the field.

# Current Story Quality Measures
In this section, I will quickly run through the current approaches to evaluate a story generated by a generative model. I will also try to lay out why I think researchers could profit from the addition of the AI Story Scale to the arsenal of evaluation metrics.

## Automatic Evaluations

Automatic evaluations are a common approach to assess the performance of language models. These evaluations typically involve comparing the output of a model to a reference or "ground truth" text. Here are some of the most commonly used automatic evaluation metrics:

### N-gram Overlap Metrics

Metrics such as BLEU ([Papineni et al., 2002](https://aclanthology.org/P02-1040.pdf)), ROUGE ([Lin, 2004](https://www.aclweb.org/anthology/W04-1013.pdf)), and METEOR ([Banerjee & Lavie, 2005](https://www.aclweb.org/anthology/W05-0909.pdf)) compare the generated text against a reference text by measuring the overlap of n-grams (contiguous sequence of n items from a given sample of text). These metrics were originally designed for machine translation and are useful for measuring the fit of the generated story against a gold standard. However, they primarily focus on surface-level text features and may not fully capture the quality of generated stories.

### Context and Reasoning Metrics

More recent evaluation methods such as LAMBADA ([Paperno et al., 2016](https://www.aclweb.org/anthology/P16-1144/)), HellaSwag ([Zellers et al., 2019](https://arxiv.org/pdf/1905.05664.pdf)), and PIQA ([Bisk et al., 2020](https://arxiv.org/pdf/1911.11641.pdf)) aim to test a model's ability to capture broader context and common sense reasoning abilities. LAMBADA evaluates a model's ability to predict the final word in a sentence given its context, while HellaSwag and PIQA test a model's ability to make common sense predictions. While these methods provide interesting insights into a model's reasoning abilities, they don't directly evaluate the quality of generated stories.

### Utility and Limitations of Automatic Evaluations
Automatic Evaluations offer the advantage of being quick, scalable, and objective. However, while these evaluations are valuable tools in the assessment of language models, they have limitations when it comes to evaluating the quality of generated stories. They often focus on specific aspects of language generation and may not fully capture the richness, creativity, and narrative coherence that are crucial in storytelling. This is where human evaluation and the AI Story Scale come into play.

## Measures Based On Human Evaluation
A different approach is to use human judges to evaluate a story ([Purdy et al., 2018](https://www.aaai.org/ocs/index.php/AIIDE/AIIDE18/paper/viewPaper/18106); [Yao et al., 2019](https://ojs.aaai.org/index.php/AAAI/article/view/4726/4604);  [Castricato et al., 2021a](https://arxiv.org/pdf/2104.07472.pdf); [Castricato et al., 2021b](https://par.nsf.gov/servlets/purl/10249509); [Callan & Foster, 2021](http://ceur-ws.org/Vol-3105/paper9.pdf)). After all, the end goal of story generation by language models is to produce convincing and engaging stories that people like to read and enjoy. Is it not natural then to use humans as our ultimate measure of story quality?

Personally, I believe that human evaluation of AI-generated stories deserves serious attention. It could be used to not only measure the 'overall quality' of stories, but also to help understand what _kind_ of stories different models are likely to produce and how they differ. It could also be used to explore how story quality changes across generations as we tweak a model's architecture or hyperparameters.

The existing measures represent an important first step for capturing how humans experience stories written by language models. However, I think they could benefit from being further refined and extended. But let's not get ahead of ourselves. Before we review existing instruments for human evaluation, let us establish what we would actually want from a scale measuring subjective story experience first.

# How Do You Measure Opinions, Anyway?
As it turns out, measuring anything from pesky humans is messy. Especially when it comes to internal states. By internal states, I mean the human experience that are not _directly_ accessible by observation. These are strange things like mood, opinions, attitudes, beliefs, or preferences. To make it sound even more complicated than it already is, psychologists call these things 'latent constructs' (or just 'constructs') or 'latent variables'. Latent variables are not directly observable, but have to be inferred from other observations – for example, what option someone picks on a question like “On a scale from 1 to 5, how interesting is this story?”.

One might think that the way we measure these variables would be straightforward: We want to know how interesting the story is. So, we just ask a person how interesting they found the story and then average that across all participants. Done, let's move on!

However, measuring latent variables comes with its own unique challenges; challenges that researchers not familiar with the peculiarities of measuring internal states might be unaware of. However, ignore these issue at your own peril! _Careless measurement of internal states can lead to very biased and potentially meaningless results!_

Luckily, there is a field that has studied this issue for decades: psychometrics.It is a discipline that has developed various tools to measure latent constructs, as well as a rich theory on the kinds of errors that can occur in these measurements and how to reduce them (for an introduction see [Furr, 2011](https://methods.sagepub.com/book/scale-construction-and-psychometrics-for-social-and-personality-psychology); [El-Den et al., 2020](https://onlinelibrary.wiley.com/doi/pdfdirect/10.1111/ijpp.12600); [Flake & Fried, 2020](https://journals.sagepub.com/doi/full/10.1177/2515245920952393)). I would urge AI researchers to take measuring human evaluations seriously and to take the lessons learned by psychometrics to heart. This way, AI research could profit from decades of hard work by psychologists and statisticians to improve how we measure what matters to humans – like the quality of AI-generated stories.

## Potential Issues In Measuring Latent Constructs
Insights from measurement theory can help us to be cognizant of potential pitfalls when measuring latent constructs. Consider first, what is implicitly assumed when we measure something like 'interestingness' by asking “On a scale from 1 to 5, how interesting is this story?”:
* We assume that when humans read stories, something like interestingness exists in their mind as a criterion for judging the story (if it does not exist, what are you measuring?).
* We assume that perceived interestingness is abstract and not directly observable. Unfortunately, there is no little sign lightning up after a person reads a story, saying “For me this story has an interestingness of 3.57”. However, we believe perceived interestigness can be measured by asking the person appropriate questions about it.
* We assume that when a person answers the question “How interesting is this story?” the perceived interestingness causes at least part of the response.[^3]
     * _We usually assume that there can be other additional causes for the response. But we will typically consider these to be randomly fluctuating measuring error. For example, a person might give a higher rating because she is in a good mood, generally gives high ratings on questionnaires, etc…_

[^3]: This model of measurement is known as the reflective measurement model: Constructs are assumed to cause indicators (responses to questions). The flip side would be a formative measurement model. However, I consider a reflective measurement model to be more appropriate for the assumptions researchers imply when collecting human evaluations, and I will therefore not give further consideration to the formative measurement model.

Problems with this process can arise at different points, but are generally put under two categories: Validity and reliability.

Both concepts have many aspects, and I cannot possibly cover the full spectrum of research on these topics here. Below, I will just give a fairly simplistic summary of the main ideas. For a more detailed coverage see for example [Drost (2011)](https://www3.nd.edu/~ggoertz/sgameth/Drost2011.pdf), [Wolming and Wikström (2010)](https://www.researchgate.net/profile/Simon-Wolming/publication/233213201_The_concept_of_validity_in_theory_and_practice/links/552627b60cf295bf160eccb5/The-concept-of-validity-in-theory-and-practice.pdf) and [Meyer (2010)](https://www.amazon.de/dp/B005NJUAK8/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1).

### Validity
A _valid_ instrument measures the construct it actually intends to measure. An _invalid_ measure does not provide measurement of the intended construct. Issues with validity can arise for a multitude of reasons.

For example, people might simply not consider 'interestingness' its own independent criterion when judging stories. That is, while it might have appeared plausible in theory, interestingness might turn out to not meaningfully exist as a construct in the real world. Responses to the question “How interesting is this story?” might instead be predicted by a mixture of other factors (for example, the perceived creativity of the story).

Alternatively, 'interestingness' might be a meaningful construct in the real world, but our questions for whatever reason simply fail to capture it and measure something else instead. Say, we tried to measure 'interestingness' by asking, “Was this story nail-biting?”. The question might turn out to measure a combination of tone and pace instead.

Measures with questionable validity are a **serious** threat to the integrity of research results [(Flake & Fried, 2020)](https://journals.sagepub.com/doi/full/10.1177/2515245920952393)! Even worse, whole fields can be led astray, if theoretical frameworks are built upon results from invalid measures. Imagine optimizing models to produce 'interesting' stories, when all measures for 'interestingness' turn out to be invalid (i.e., measuring something else). Models will be optimized for _something_, but for what exactly will be very poorly understood.

### Reliability

A _reliable_ measure captures whatever it measures with precision. If we use it repeatedly on the same object, we can expect to get a similar result each time with little measurement error. An _unreliable_ instrument lacks precision, and might be basically useless if the issue is severe. That is, reliability describes the degree of measurement error of a measure.

If the scores we are getting from a measure vary wildly, it might not matter whether it does measure what it should measure or not – we simply cannot trust the results we are getting. In other words, we want a measure to be valid _and_ reliable.

<img src="https://upload.wikimedia.org/wikipedia/commons/5/5d/Reliability_and_validity.svg" alt="loss graph" width="400"/></br>

_[© Nevit Dilmen](https://commons.wikimedia.org/wiki/File:Reliability_and_validity.svg)_

## How To Ensure Validity And Reliability
So, how do we make sure that our measure for human ratings is valid and reliable? The answer is generally: By using psychometric techniques for validating questionnaires with real-world data.

Ideally, a systematic and rigorous approach is taken starting from the construction of the measure. A good summary of best practices according to insights from psychometric research can for example be found in [Boateng et al. (2018)](https://www.frontiersin.org/articles/10.3389/fpubh.2018.00149/full) and [Hinkin (1998)](https://journals.sagepub.com/doi/abs/10.1177/109442819800100106).

A very brief (and likely overly superficial) overview of the process:
1. _Item Generation_: Define the dimensions to be measured. Then generate items for these dimensions. Base those on existing literature and theory and/or on exploratory research (= talking to people). Note that the assumed dimensions are tentative at this point and likely will have to be revised once your theory collides with real-world data. Humans are pesky – they ~~might~~ will react differently to your items than your nice, clean theory suggests.
2. _Scale Development_: Take your drafted questionnaire and see how people respond to your questions in the real world. The main technique here is analyzing responses to the questions with exploratory factor analysis (EFA) to investigate the underlying factorial structure that explains response patterns on the items. Usually, this step is also used to sort out items that are undesirable for one reason or another.
Ideally, the first version of the questionnaire will be finalized at the end of this step: The researcher will typically have revised the dimensions to be measured and will have selected the ideal set of items to measure those for a first usable version of the scale.
3. _Scale Validation_: Undertake additional studies to validate the scale's validity and reliability. You might want to suggest modifications to the questionnaire based on your results to further refine the measure.

# Existing Measures For Human Evaluations Of Stories: A Second Look
We have now covered enough ground, to discuss the potential issues of existing measures for story quality. In short, I see methodological shortcomings and potentially severe issues with the existing measures.

To my awareness, _none_ of the instruments for human evaluations of AI-generated stories have been evaluated on whether they actually measure anything meaningful (testing validity) or for their precision (testing reliability). As I have just discussed, this represents a _serious_ threat to the usefulness of these measures.

Furthermore, it is very common in the field for each concept (such as 'local contextuality' or 'enjoyability') to be measured with a single item (e.g., [Purdy et al., 2018](https://www.aaai.org/ocs/index.php/AIIDE/AIIDE18/paper/viewFile/18106/17228); [Yao et al., 2019](https://ojs.aaai.org/index.php/AAAI/article/view/4726/4604); [Callan & Foster, 2021](http://ceur-ws.org/Vol-3105/paper9.pdf)). Measuring fairly abstract latent constructs with only one item is known to come at severe psychometric costs ([Furr, 2011](https://methods.sagepub.com/book/scale-construction-and-psychometrics-for-social-and-personality-psychology)): For one, single items are likely to be very imprecise and not capture the full breadth of the construct. Maybe more importantly, many techniques to evaluate the quality of the measure are unavailable or difficult with a single item.[^4] For these reasons, established psychometric guidelines generally recommend 4–6 items per construct for a reliable psychometric evaluation and measurement (e.g., [Hinkins et al., 1998](https://journals.sagepub.com/doi/abs/10.1177/109442819800100106)).

[^4]: Admittedly, this does not matter much in this case, as none of these items have ever been checked for their psychometric quality.

The existing instruments have clearly laid the groundwork for evaluating the quality and nature of AI-generated stories. But as we have seen in the previous section, they currently do so at the risk of producing biased results and misleading theoretical insights. While I do not want to take away from their work, I believe they would benefit from being more thoroughly validated against established psychometrics principles.

# Enter The AI Story Scale
My proposed instrument for evaluating AI-generated stories was developed according to best practices for scale construction: The AI Story Scale (AISS). It is currently the only questionnaire for rating AI-generated stories based on empirical analysis. It should provide a robust instrument to understand how different language models and hyperparameters influence people's experience of the resulting story output. You can find the instrument [here](https://github.com/MWiechmann/ai_story_scale/tree/main/AISS).

I will try to slowly improve and expand this scale with new data.[^4] Links to my studies on the AISS:

[^4]: However, when I say 'slow', I mean _really slow_ – this is still a hobby project of mine!

## [Study 1: Building the AI Story Scale](https://github.com/MWiechmann/ai_story_scale/tree/main/study1_scale_construction)
The initial study for drafting the items for the AISS, and exploring their factorial structure. Based on the results of this study, I constructed the version of the AISS.

It also contains a few Proof of Concept analyzes to show how the AISS can be used to gain a more detailed understanding of how different generation settings can lead to different types of stories.

# How To Cite The AISS
Go to the [main page of the repo](https://github.com/MWiechmann/ai_story_scale) if you aren't there already, and look to the right to the 'About' field. Click the line that says 'Cite this repository'.

# FAQ
## What do you mean, there is no scale for human evaluations of AI-generated stories? I have seen a few!
That is not what I said. I said there are no scales that have been _psychometrically validated_. I am aware of a few instruments that have been used to evaluate AI-generated stories. However, _none_ of them have been evaluated for their psychometric quality. We do not know what criteria most people use when answering questions from those scales, and if those criteria match the intentions of the authors of the respective scale. We do not know how reliable the results from the scales are. This is a serious issue, as it means that we cannot be sure that the results we get from these instruments are actually meaningful. For a primer on those issue, reread [this section](#potential-issues-in-measuring-latent-constructs) and have a look at the references I have linked.

Of course, if I am wrong and some scale has been psychometrically validated for AI research, I would be thrilled to hear about it. Please, please, _please_ let me know!

## Why do you ask for evaluations from single stories? You should do pairwise comparisons of stories!
Pairwise comparisons represent a different research design with different weaknesses and strengths. Choosing between a pairwise comparison design versus evaluations of single stories should therefore depend on the research question at hand. Advising _only_ pairwise comparisons _always_, seems very ill-advised to me, however.

Pairwise comparisons will give you dichotomous data (Story chosen? A/B). Dichotomous data by definition carries less information than a choice from, say, a 5-point Likert scale. This means you necessarily have to sacrifice some statistical power with such a design (or rather, you will be limited to analysis methods with lower statistical power).

Furthermore, choices from pairwise comparison are even harder to probe for the underlying constructs that explain the answers. _Why_ did the participants select one story over the other? What criteria did they use? What did they like about one story and dislike about the other? These are questions that are very difficult to answer when all you have is a single choice of story A versus story B.

I also want to point out that just because you are using a pairwise comparison design, this does not somehow relieve you of the duty to psychometrically validate your human evaluations. That is, psychometric measurements still need to be checked for their validity and reliability if you hope to conduct research with any shred of scientific rigor. What latent factors determine the choice of story A over story B? Does this match with what you intended to measure (validity)? How reliable are the results? Do raters generally agree on the same story being better than the other (reliability)? Validity can be very difficult to check with a pairwise comparison design, while reliability _could_ be controlled for relatively easily with measures for inter-rater reliability (most of those measures could be calculated by hand if need be). Yet, I have not encountered a single paper from AI research that has reported _any_ psychometric analysis of their instrument.

Of course, I am not saying that you should never use pairwise comparison designs. There are strengths of such designs: The measures a closer to a “behavioral” measure, as people actually chose one story over the other. This is an advantage if you are interested in studying or predicting behavior (such as picking one model over another). However, many theories will make many explicit or implied assumptions about the underlying attributes of stories that lead to such a choice. If you want to test these theories, you need to be able to measure these attributes. Pairwise comparisons will often not be the ideal study design for this.

## Why do you evaluate such long excerpt? People need time to process the story, and are really bad at getting the big picture and spotting plot holes. You should use short snippets instead!
If you want to study logical inconsistencies within short snippets, use short snippets. I am interested in more global impressions from AI-generated texts. Therefore, I initially used longer excerpts. 

I disagree though that people are bad at getting a big picture from stories. I think if you let people read a somewhat longer excerpt (e.g. a 5 minute-read) from a story written by language model, they will walk away with a certain impression of that text. This impression will differ depending on the peculiarities of the model used to generate the excerpt. I think those differences are interesting and meaningful to study, and it would be unfortunate if those differences were never studied because all that is ever looked at are short snippets.

I would argue that my data agrees with me, btw: For evaluations of longer story excerpts, I found plenty of variance in the data that clusters meaningfully around certain story factors.
