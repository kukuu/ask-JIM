# "Ask-JIM"

(Author: _Alexander Adu-Sarkodie_)


The **JIM AI Engine** is a unique custom domain based AI, LLM, NLP, ML, RAG pipeline orchestrator.  

It's  backend server component leverages the core LLM-NLP-RAG pipeline through a sophisticated multi-layered algorithm that processes natural language queries against real-time energy data. The pipeline begins with an HTTP POST endpoint (/api/llm/query) that receives user questions and employs pattern-matching NLP to categorize queries into specific analytical domains - statistical analysis, load forecasting, performance evaluation, or tariff optimization. 

When a query contains statistical keywords like "stat" or "analysis," **JIM** executes a true RAG pipeline by querying Supabase for the latest 50 meter readings, then performs real-time aggregation to calculate averages, maximums, and minimums per meter. For load-related queries, the engine simulates predictive scenarios using the same consumption algorithms that generate live meter data, applying 20-25% load increases and calculating corresponding cost impacts based on time-of-use tariff structures.

The RAG component dynamically constructs context by analysing temporal patterns from the database, identifying peak consumption hours (2:00 PM - 6:00 PM) and correlating them with tariff rates. For performance optimization queries, **JIM** implements anomaly detection by comparing meter fluctuations against baseline consumption patterns, flagging Meter 3's peak-hour spikes as optimization targets.

The pipeline's intelligence is enhanced by the server component file's real-time data simulation, which models UK electricity usage patterns with peak-hour multipliers (1.5x-2x normal consumption) and overnight reductions (50-70%). This simulated data provides the training context for **JIM**'s analytical responses, enabling it to make evidence-based recommendations like load shifting strategies that could yield 10-15% savings.

**JIM**'s response generation employs dynamic templated HTML output with structured data visualisation, presenting findings through categorised statistics, bullet-point recommendations, and cost-impact analyses. The system maintains conversation context through timestamped question-answer pairs while enforcing data freshness by always querying the most recent 50 records.

The algorithm expects continuous real-time data ingestion from the WebSocket layer, which generates new readings every 2 seconds and persists them to Supabase every 60 seconds. This ensures **JIM**'s analyses are always based on current system states rather than historical data alone. The health check endpoint (/health) provides pipeline monitoring, verifying both the LLM service availability and underlying data connectivity.

Ultimately, **JIM** transforms the server component's  simple data simulator into an intelligent energy analytics platform by combining real-time data processing, pattern recognition, predictive modeling, and natural language understanding - all while maintaining the low-latency requirements essential for interactive energy management decision support.

This work epitomises technical depth of engineering systems thinking in Computer Science, encapsulating Artificial Intelligence, Machine Learning, Large Language Modelling, Natural Language Processing, Mathematics and Physics brought together.

To see it in action kindly visit and log into **SPYDER**  https://www.energytariffscheck.com/ and its designated  **NEWSLETTER** section - https://www.energytariffscheck.com/newsletter .


**Portfolio**: https://github.com/kukuu/portfolio/blob/main/README.md


