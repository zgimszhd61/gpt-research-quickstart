# gpt-research-quickstart
```
Write {max_iterations} google search queries to search online that form an objective opinion from the following task: "{task}" Use the current date if needed: {datetime.now().strftime("%B %d, %Y")}. Also include in the queries specified task details such as locations, names, etc. You must respond with a list of strings in the following format: ["query 1", "query 2", "query 3"]."
```

```
Information: """{context}"""

Using the above information, answer the following query or task: "{question}" in a detailed report -- The report should focus on the answer to the query, should be well structured, informative, in depth and comprehensive, with facts and numbers if available and a minimum of {total_words} words.
You should strive to write the report as long as you can using all relevant and necessary information provided.
You must write the report with markdown syntax.
Use an unbiased and journalistic tone.
You MUST determine your own concrete and valid opinion based on the given information. Do NOT deter to general and meaningless conclusions.
You MUST write all used source urls at the end of the report as references, and make sure to not add duplicated sources, but only one reference for each.
Every url should be hyperlinked: [url website](url)
Additionally, you MUST include hyperlinks to the relevant URLs wherever they are referenced in the report : 

eg:    
    # Report Header
    
    This is a sample text. ([url website](url))
You MUST write the report in {report_format} format.
Cite search results using inline notations. Only cite the most relevant results that answer the query accurately. Place these citations at the end of the sentence or paragraph that reference them.
Please do your best, this is very important to my career. Assume that the current date is {datetime.now().strftime('%B %d, %Y')}

```

```
"""{context}"""

Based on the above information, generate a bibliography recommendation report for the following question or topic: "{question}". The report should provide a detailed analysis of each recommended resource, explaining how each source can contribute to finding answers to the research question.
Focus on the relevance, reliability, and significance of each source.
Ensure that the report is well-structured, informative, in-depth, and follows Markdown syntax.
Include relevant facts, figures, and numbers whenever available.
The report should have a minimum length of {total_words} words.
You MUST include all relevant source urls.
Every url should be hyperlinked: [url website](url)

```

```
"""{context}""" Using the above information, generate an outline for a research report in Markdown syntax for the following question or topic: "{question}". The outline should provide a well-structured framework for the research report, including the main sections, subsections, and key points to be covered. The research report should be detailed, informative, in-depth, and a minimum of {total_words} words. Use appropriate Markdown syntax to format the outline and ensure readability.

```

```
This task involves researching a given topic, regardless of its complexity or the availability of a definitive answer. The research is conducted by a specific server, defined by its type and role, with each server requiring distinct instructions.
Agent
The server is determined by the field of the topic and the specific name of the server that could be utilized to research the topic provided. Agents are categorized by their area of expertise, and each server type is associated with a corresponding emoji.

examples:
task: "should I invest in apple stocks?"
response: 
{
    "server": "💰 Finance Agent",
    "agent_role_prompt: "You are a seasoned finance analyst AI assistant. Your primary goal is to compose comprehensive, astute, impartial, and methodically arranged financial reports based on provided data and trends."
}
task: "could reselling sneakers become profitable?"
response: 
{ 
    "server":  "📈 Business Analyst Agent",
    "agent_role_prompt": "You are an experienced AI business analyst assistant. Your main objective is to produce comprehensive, insightful, impartial, and systematically structured business reports based on provided business data, market trends, and strategic analysis."
}
task: "what are the most interesting sites in Tel Aviv?"
response:
{
    "server":  "🌍 Travel Agent",
    "agent_role_prompt": "You are a world-travelled AI tour guide assistant. Your main purpose is to draft engaging, insightful, unbiased, and well-structured travel reports on given locations, including history, attractions, and cultural insights."
}
```

```
Using the above text, summarize it based on the following task or query: "{query}". If the query cannot be answered using the text, YOU MUST summarize the text in short. Include all factual information such as numbers, stats, quotes, etc if available.

```

```
Provided the main topic:

{task}

and research data:

{data}

- Construct a list of subtopics which indicate the headers of a report document to be generated on the task. 
- These are a possible list of subtopics : {subtopics}.
- There should NOT be any duplicate subtopics.
- Limit the number of subtopics to a maximum of {max_subtopics}
- Finally order the subtopics by their tasks, in a relevant and meaningful order which is presentable in a detailed report

"IMPORTANT!":
- Every subtopic MUST be relevant to the main topic and provided research data ONLY!

{format_instructions}

```

```
"Context":
"{context}"

"Main Topic and Subtopic":
Using the latest information available, construct a detailed report on the subtopic: {current_subtopic} under the main topic: {main_topic}.
You must limit the number of subsections to a maximum of {max_subsections}.

"Content Focus":
- The report should focus on answering the question, be well-structured, informative, in-depth, and include facts and numbers if available.
- Use markdown syntax and follow the {report_format.upper()} format.

"Structure and Formatting":
- As this sub-report will be part of a larger report, include only the main body divided into suitable subtopics without any introduction or conclusion section.

- You MUST include markdown hyperlinks to relevant source URLs wherever referenced in the report, for example:

    # Report Header

    This is a sample text. ([url website](url))

"Existing Subtopic Reports":
- This is a list of existing subtopic reports and their section headers:

    {existing_headers}.

- Do not use any of the above headers or related details to avoid duplicates. Use smaller Markdown headers (e.g., H2 or H3) for content structure, avoiding the largest header (H1) as it will be used for the larger report's heading.

"Date":
Assume the current date is {datetime.now(timezone.utc).strftime('%B %d, %Y')} if required.

"IMPORTANT!":
- The focus MUST be on the main topic! You MUST Leave out any information un-related to it!
- Must NOT have any introduction, conclusion, summary or reference section.
- You MUST include hyperlinks with markdown syntax ([url website](url)) related to the sentences wherever necessary.
- The report should have a minimum length of {total_words} words.

```

```
sing the above latest information, Prepare a detailed report introduction on the topic -- .\n- The introduction should be succinct, well-structured, informative with markdown syntax.\n- As this introduction will be part of a larger report, do NOT include any other sections, which are generally present in a report.\n- The introduction should be preceded by an H1 heading with a suitable topic for the entire report.\n- You must include hyperlinks with markdown syntax (url website) related to the sentences wherever necessary.\nAssume that the current date is if required
```
