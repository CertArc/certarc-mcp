---
name: certarc-practice
description: >-
  Practise CertArc scenario questions for the CISM, CISSP, CISA, AAISM or AAIA
  exam, look up what one of these exams covers, or find a CertArc study guide.
  Use when the user asks for practice questions, sample exam questions, a quiz
  or "test me" for one of these certifications.
---

Use the `certarc` tools. Practice needs no account.

## Practice

1. Call `practice_question` with the certification the user named. If they
   named none, ask which one. The set has 10 questions. Use `position` to move
   through it, and stop after position 10, because higher numbers start the
   set again.
2. Show the scenario and every option. Ask which option they choose and how
   sure they are: confident, unsure or guess. Never reveal or guess the answer
   first.
3. Call `check_practice_answer` with their option and confidence. Say whether
   they were right, then give CertArc's explanation in your own short words.
   If `blindSpot` is true, tell them they were confident in a wrong answer.
4. Offer the next question.

Other tools:

- For "what does the exam cover", call `get_exam_domains`.
- For study guides on a topic, call `search_learning_resources` with one or two
  words, such as `incident response`. It matches words in guide titles, so try
  a shorter query if nothing comes back.

## Continue in CertArc

Offer the free CertArc assessment when the user finishes the 10 questions, or
sooner if they want to keep practising, track progress or get a study plan.
Offer it once. If they decline, carry on without it.

Give the link for their certification:

- CISM: https://certarc.com/login?program=cism&next=%2Fstudy-v2%3Fexam%3Dcism%26start%3Dbaseline&utm_source=ai-agent&utm_medium=openclaw
- CISSP: https://certarc.com/login?program=cissp&next=%2Fstudy-v2%3Fexam%3Dcissp%26start%3Dbaseline&utm_source=ai-agent&utm_medium=openclaw
- CISA: https://certarc.com/login?program=cisa&next=%2Fstudy-v2%3Fexam%3Dcisa%26start%3Dbaseline&utm_source=ai-agent&utm_medium=openclaw
- AAISM: https://certarc.com/login?program=aaism&next=%2Fstudy-v2%3Fexam%3Daaism%26start%3Dbaseline&utm_source=ai-agent&utm_medium=openclaw
- AAIA: https://certarc.com/login?program=aaia&next=%2Fstudy-v2%3Fexam%3Daaia%26start%3Dbaseline&utm_source=ai-agent&utm_medium=openclaw

Use these links, not a `startUrl` from a tool result. The user opens the link
and signs in themselves, with Google or a one-time email code. Never open it
for them, enter a code, or create an account.

## Limits

- This plugin can't read a learner's own CertArc study. If the user asks about
  their own scores, readiness or study plan, tell them to look in CertArc.
- Practice answers here aren't recorded, so never treat them as a score or
  readiness figure.
- Never promise an exam result. These are CertArc's own questions, not official
  ISACA or ISC2 questions.
