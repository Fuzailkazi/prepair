# Automated Meeting Prep Framework

## Title
Automated Meeting Prep Framework

## Goal
Transform a raw company input into a complete Meeting Prep Dashboard with research artifacts, media, and an HTML interface.

## Trigger Details
Inputs may come from Zapier, CRM, email, or manual prompts with company_name and optional meeting metadata.

## Phase 0: Agent Pre-Research (Data Enrichment)
Initial research phase to gather high-quality seed data before using NotebookLM.

## Step 0.1 Website Scrape
Scrape company website pages such as About, Products, Pricing, Team, Blog, and Careers.

## Step 0.2 External Enrichment
Gather LinkedIn, Crunchbase, news, Wikipedia, Glassdoor, and YouTube information.

## Step 0.3 Synthesize Company Profile
Combine all gathered data into a structured company profile with leadership, funding, products, competitors, and recent news.

## Phase 1: Notebook Preparation & Initial Ingestion
Create a dedicated NotebookLM workspace for the company.

## Step 1.1 Create Notebook
mcp: notebook_create with title 'Meeting Prep - [Company Name]'.

## Step 1.2 Inject Seed Data as Text Source
Add synthesized company profile as a text source.

## Step 1.3 Add Scraped URLs as Sources
Add high-quality URLs individually (3–8 recommended).

## Phase 2: Autonomous Deep Research
Use NotebookLM web research to discover dozens of sources.

## Step 2.1 Start Deep Research
Run research_start with deep mode for exhaustive coverage.

## Step 2.2 Poll Until Complete
Poll research_status until status is completed.

## Step 2.3 Batch Import Sources
Import research sources in batches of 20 to avoid timeouts.

## Phase 3: Artifact Generation & Extraction
Generate artifacts using notebook queries and studio tools.

## Step 3.1 Executive Briefing
Generate executive pre-meeting briefing document.

## Step 3.2 Deep Research Report
Generate deep research industry trend report.

## Step 3.3 Competitive Intelligence
Generate competitive intelligence cheat sheet.

## Step 3.4 Market Infographic
Generate a portrait infographic of the market landscape.

## Step 3.5 Audio Briefing Podcast
Generate an AI audio podcast briefing.

## Step 3.6 Knowledge Quiz
Generate an 8-question knowledge quiz.

## Step 3.7 Flashcards
Generate flashcards and regenerate if fewer than 8 cards.

## Step 3.8 Slide Deck
Generate a detailed slide deck if required.

## Phase 4: Index File Generation
Create 00_INDEX.md summarizing all artifacts and usage instructions.

## Phase 5: Premium HTML Dashboard
Build a premium dark-mode HTML dashboard with tabs, markdown rendering, quiz UI, flashcards, and infographic.

## Guiding Principles
Design rules and operational constraints for the system.

## Batch Imports Rule
Always import deep research sources in chunks of 20.

## Fail Gracefully
If generation artifacts fail or are incomplete, regenerate or skip gracefully.

## Aesthetics Requirement
Dashboard must look premium with dark UI, glassmorphism, and animations.

## Data Isolation
Each client meeting must use its own NotebookLM notebook.

## Security
Never expose API keys or credentials in generated artifacts.

## File Naming Convention
00_INDEX.md, 01_briefing_doc.md, 02_deep_research_report.md, 03_competitive_intel.md, 04_market_infographic.png, 06_pre_call_quiz.md, 07_flashcards.md, 08_slide_deck.pdf, audio_briefing.mp3, index.html
