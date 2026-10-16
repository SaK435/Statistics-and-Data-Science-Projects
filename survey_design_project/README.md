# Survey Design Project: Students' Nationality and Perceptions of Social Media in Political Debate

Group project for the Survey Methodology course as part of my MSc in Statistics & Data Science at Leiden University. The project covers the full questionnaire design stage: research question, operationalization, questionnaire construction, peer review and cognitive interviewing.

**Team:** group of 2 students.

## Research question
Is there a relationship between how students perceive the role of social media in political debate and their nationality? The null hypothesis is that nationality has almost no effect on this perception when assessed alongside other major features.

## Design at a glance
- **Population:** (international) college students at Leiden University
- **Construct:** perception of the role of social media in political debate, measured on a Likert scale from social media alarmist to social media supporter, plus self-reported online political participation
- **Covariates:** field of study, education level, age, gender and social media use (platforms and frequency)
- **Design logic:** because nationality cannot be influenced by the respondent, the aim is to evaluate how much it matters compared to other core variables. The path diagram in `figures/` shows the assumed relationships, including the check for colliders.

## What testing changed
Peer review and a cognitive interview led to concrete changes:
- Added definitions of politics, debate and social media (with examples of what counts) after respondents found these terms unclear
- Added YouTube and Reddit to the platform list to avoid many "Other" answers
- Split overly broad questions into sub-questions and moved to a Likert scale, because respondents could agree with several answer options at once
- Replaced "verified/official sources" with "governmental sources" in the news source question
- Made the main questions and the analysis plan more specific, and added further references in APA format

Full details: [02_lessons_learned_peer_review_and_cognitive_interview.pdf](02_lessons_learned_peer_review_and_cognitive_interview.pdf)

## Planned analysis
- Descriptive statistics (univariate and bivariate) to understand the data first
- Chi-squared association tests between categorical variables, for example, nationality and whether social media is used for politics
- Regression model to estimate the contribution of nationality while accounting for the other covariates

## Limitations identified
- No sampling list of Leiden students, so probability sampling is difficult
- Some nationalities are underrepresented or absent, which can bias results
- Respondents with less internet access are harder to reach
- International students may hold different political opinions than they would in their home country
- Answers could depend on whether elections took place recently

## Files
- [01_research_design.pdf](01_research_design.pdf): topic, research question, operationalization, planned analyses and constraints (to be added)
- [02_lessons_learned_peer_review_and_cognitive_interview.pdf](02_lessons_learned_peer_review_and_cognitive_interview.pdf) (to be added)
- `figures/`: path diagram and construct operationalization
- Final questionnaire: to be added

## Status
[State plainly, for example: "Design stage only. The survey was not fielded, so no results are reported." Or describe what happened if it was fielded.]
