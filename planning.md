# Project 1 Planning: The Unofficial Guide

> Write this document before you write any pipeline code.
> Your spec and architecture diagram are what you'll use to direct AI tools (Claude, Copilot, etc.) to generate your implementation — the more specific they are, the more useful the generated code will be.
> Update the Retrieval Approach and Chunking Strategy sections if you change your approach during implementation.
> Update this file before starting any stretch features.

---

## Domain

<!-- What domain did you choose? Why is this knowledge valuable and hard to find through official channels? -->
The domain of this project is student-generated reviews and experiences regarding Mathematics and Computer Science professors at Denison University. This knowledge is valuable because it provides insights into the teaching styles, course difficulty, and overall student satisfaction with professors that may not be fully captured in official course descriptions or ratings. It is hard to find through official channels because official university resources often lack detailed, candid feedback from students, and platforms like RateMyProfessors may not have comprehensive or up-to-date information for all professors at Denison University.

---

## Documents

<!-- List your specific sources: URLs, subreddit names, forum threads, or file descriptions.
     Aim for at least 10 sources that together cover different subtopics or perspectives within your domain. -->

| # | Source | Description | URL or location |
|---|--------|-------------|-----------------|
| 1 | Denison University | A general overview of Matthew Neal's profile and his academic background, field of interests | https://denison.edu/people/matthew-neal |
| 2 | Denison University | A general overview of Sarah Wolff's profile and her academic background, field of interests | https://denison.edu/people/sarah-wolff |
| 3 | Denison University | A general overview of Adam Waterbury's profile and his academic background, field of interests | https://denison.edu/people/adam-waterbury |
| 4 | Denison University | A general overview of Robert Viator's profile and his academic background, field of interests | https://denison.edu/people/robert-viator |
| 5 | Denison University | A general overview of Lew Ludwig's profile and his academic background, field of interests | https://denison.edu/people/lew-ludwig |
| 6 | Denison University | A general overview of David Kahn's profile and his academic background, field of interests | https://denison.edu/people/david-kahn |
| 7 | Denison University | A general overview of Flannery Currin's profile and her academic background, field of interests | https://denison.edu/people/flannery-currin |
| 8 | Denison University | A general overview of Mikey Goldweber's profile and his academic background, field of interests | https://denison.edu/people/mikey-goldweber |
| 9 | Rate My Professor | Student reviews and ratings for Matthew Neal | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123456 |
| 10 | Rate My Professor | Student reviews and ratings for Sarah Wolff | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123457 |
| 11 | Rate My Professor | Student reviews and ratings for Adam Waterbury | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123458 |
| 12 | Rate My Professor | Student reviews and ratings for Robert Viator | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123459 |
| 13 | Rate My Professor | Student reviews and ratings for Lew Ludwig | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123460 |
| 14 | Rate My Professor | Student reviews and ratings for David Kahn | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123461 |
| 15 | Rate My Professor | Student reviews and ratings for Flannery Currin | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123462 |
| 16 | Rate My Professor | Student reviews and ratings for Mikey Goldweber | https://www.ratemyprofessors.com/ShowRatings.jsp?tid=123463 |

---

## Chunking Strategy

<!-- How will you split documents into chunks?
     State your chunk size (in tokens or characters), overlap size, and explain why those
     numbers fit the structure of your documents.
     A review-heavy corpus warrants different chunking than a long FAQ. -->

**Chunk size:** 250-300 tokens

**Overlap:** 50 tokens

**Reasoning:** Professor reviews are typically short opinion-based texts. Large chunks may combine multiple unrelated comments and dilute retrieval quality. A chunk size of 250-300 tokens allows for capturing individual reviews or comments while maintaining enough context. An overlap of 50 tokens ensures that if a review is split between two chunks, the relevant information is still retained in both, improving retrieval accuracy.

---

## Retrieval Approach

<!-- Which embedding model are you using (e.g., all-MiniLM-L6-v2 via sentence-transformers)?
     How many chunks will you retrieve per query (top-k)?
     If you were deploying this for real users and cost wasn't a constraint, what tradeoffs
     would you weigh in choosing a different embedding model — context length, multilingual
     support, accuracy on domain-specific text, latency? -->

**Embedding model:**

**Top-k:**

**Production tradeoff reflection:**

---

## Evaluation Plan

<!-- List your 5 test questions with their expected correct answers.
     Questions should be specific enough that you can judge whether the system's response
     is right or wrong. "What are good dining halls?" is too vague.
     "What do students say about wait times at [dining hall name] during lunch?" is testable. -->

| # | Question | Expected answer |
|---|----------|-----------------|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |

---

## Anticipated Challenges

<!-- What could go wrong? Name at least two specific risks with reasoning.
     Consider: noisy or inconsistent documents, missing source attribution, off-topic
     retrieval, chunks that split key information across boundaries. -->

1.

2.

---

## Architecture

<!-- Draw a diagram of your pipeline showing the five stages:
     Document Ingestion → Chunking → Embedding + Vector Store → Retrieval → Generation
     Label each stage with the tool or library you're using.
     You can use ASCII art, a Mermaid diagram, or embed a sketch as an image.
     You'll use this diagram as context when prompting AI tools to implement each stage. -->

---

## AI Tool Plan

<!-- For each part of the pipeline below, describe:
     - Which AI tool you plan to use (Claude, Copilot, ChatGPT, etc.)
     - What you'll give it as input (which sections of this planning.md, which requirements)
     - What you expect it to produce
     - How you'll verify the output matches your spec

     "I'll use AI to help me code" is not a plan.
     "I'll give Claude my Chunking Strategy section and ask it to implement chunk_text()
     with my specified chunk size and overlap" is a plan. -->

**Milestone 3 — Ingestion and chunking:**

**Milestone 4 — Embedding and retrieval:**

**Milestone 5 — Generation and interface:**
