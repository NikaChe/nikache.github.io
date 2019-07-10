---
layout: post
title: "Advices for chatbot"
date: 2019-07-10
---
- Start from defining the goal of bot and what you need to achieve it
- Include small talk 
- For each intent write more then 50 examples
- Don't tag as entity every word in sentence
- Don't write sentences, that are only entities
- 

Entities extraction for chatbot RASA. Ways:

- Duckling. Duckling is a rule-based entity extraction library developed by Facebook
- CRFEntityExtractor. Extract entities defined in examples. Good for cases with a lot of date
- SpacyExtractor. Extract PER, ORG and MISC (for French), based on pretrained entities, so can be good if there is no much data



References:

1. https://towardsdatascience.com/22-rules-you-should-never-break-in-each-phase-of-bot-building-49a5636f44f7
