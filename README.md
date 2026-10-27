# 4340project

Data source: https://www.consumerfinance.gov/foia-requests/foia-electronic-reading-room/cfpb-consumer-complaint-database-narratives-archive/

Description from source: Archive of consumer complaints received December 1, 2011 through August 14, 2026 that were previously published in the Consumer Complaint Database.

The business question would be: How accurately and cost-effectively can a GenAI model classify consumer complaint narratives into product categories to support human routing?

A manageable workflow would be:
1. Prepare the data: Keep complaints with narratives. Check category counts and select three or four categories with enough examples.
2. Create an evaluation sample: Use roughly 200–300 complaints. Have both partners independently review a subset and resolve disagreements.
3. Compare approaches: Test a simple baseline against an LLM. Give the models only narrative text so existing product and issue fields cannot reveal the answer.
4. Evaluate: Report precision, recall, macro-F1, a confusion matrix, confidence intervals, response time, and cost. Measure agreement between your manual labels as well.
5. Govern: Define measurable rules for human review, unsupported outputs, and handling potentially identifying text.
This gives you material for every rubric component: a reproducible notebook, quantitative results, a governance memo, and individual AI decision logs.

Two limitations should shape the project: 97.3% of records have no narrative, so your conclusions would apply to the narrative subset. Also, the existing product label is a useful reference label, but manual review is needed to identify ambiguous cases.
