# The AI User Journey: Full Map

Nine stages, four lanes. Every line below comes from the source artifact.

Lanes:

- **User Thinking**: the internal state the user is in
- **User Action**: the observable behaviour
- **AI System**: what the system must do at that stage
- **PM Metrics**: what a product manager measures at that stage

Emotional arc across the journey: 😤 🤔 🧩 ⏳ 🔍 😕 😌 😊 🤩

---

## Stage 1. Problem Recognition

> "I need help with X" 😤

**User Thinking**

- Has a clear problem but no obvious solution in reach
- Turns to AI because the task is too slow, too complex, or outside their skill set
- May not know exactly what they want, only what pain they want removed

**User Action**

- Opens the product or navigates to the AI feature
- May already have a document, data set, or draft open
- Arrives with a specific task in mind, not a general curiosity

**AI System**

- Detects user intent from entry point signals: feature opened, document in context, session history
- Sets up the interaction context before the user types a single word
- Surfaces relevant starting points based on inferred goal

**PM Metrics**

- Entry rate: percentage of active users who initiate an AI interaction per session
- Time from product open to first AI engagement
- Intent detection accuracy before explicit input

---

## Stage 2. Intent Expression

> "Here's what I want" 🤔

**User Thinking**

- Tries to put their goal into words the AI will understand
- Unsure how specific to be: too vague gets generic output, too specific feels like over explaining
- Wonders whether to upload files, paste text, or just type

**User Action**

- Types a prompt, uploads a document, selects a template, or uses a suggested action
- Makes a judgment call about how much context to provide upfront
- Submits the first input and immediately starts second guessing it

**AI System**

- Parses the natural language intent and classifies the request type
- Identifies what information is present and what is missing
- Decides whether to proceed or ask a clarifying question

**PM Metrics**

- Prompt success rate: first prompt leads to an output the user uses
- Prompt abandonment rate: types something then deletes and closes
- Time from feature open to first submission

---

## Stage 3. Context Building

> "AI needs more info" 🧩

**User Thinking**

- Realises the AI needs more background to give a useful answer
- Weighs whether to provide more context or just see what it does
- Feels the friction of re explaining things the AI should already know

**User Action**

- Adds documents, data files, or pastes relevant background
- Answers a clarifying question the AI has asked
- Adjusts scope, format preferences, or tone before generation

**AI System**

- Retrieves relevant memory, prior outputs, user context, or connected data sources
- Asks a clarifying question if confidence in intent is low
- Signals what additional context would improve the output

**PM Metrics**

- Context completeness score before generation
- Average number of context additions before first generation
- Clarifying question acceptance rate

---

## Stage 4. Generation

> "Show me a solution" ⏳

**User Thinking**

- Waiting and hoping: this is the peak anxiety moment
- Watching the streaming text and forming an opinion before it finishes
- Mentally rehearsing what to do if the output is not useful

**User Action**

- Waits for output, watching loading state or streaming text
- Begins reading before generation is complete if text streams
- Forms an initial impression within the first 3 to 5 seconds

**AI System**

- Generates the response based on available intent and context
- Runs output through safety and quality guardrails before delivery
- Streams tokens progressively or delivers the complete output

**PM Metrics**

- Generation latency: P50 and P99 time to first token and completion
- Automated quality score from eval suite on output samples
- Output length aligned to task complexity

---

## Stage 5. Evaluation

> "Is this useful?" 🔍

**User Thinking**

- Reading critically, comparing output to their internal expectation
- Actively looking for errors, hallucinations, missing context, wrong tone
- Deciding in real time whether to use it, edit it, or start over

**User Action**

- Reads the output fully, or skims then re reads key sections
- Tests it if it is code or data: runs it, checks against the source
- Decides to accept, edit, regenerate, or abandon

**AI System**

- Collects implicit signals: scroll depth, time on output, copy events
- Infers satisfaction without requiring explicit feedback
- Logs signals as training data for future personalisation

**PM Metrics**

- Acceptance rate: output used without significant editing
- Time spent on output before first action
- Implicit signals: scroll completion, copy rate, application rate

---

## Stage 6. Correction

> "Not exactly..." 😕

**User Thinking**

- Knows roughly what was wrong but not how to express the fix
- Wondering whether to edit the output directly or re prompt
- Mild frustration but still engaged, has not given up yet

**User Action**

- Edits inline, regenerates with a modified prompt, or asks a follow up
- Tries to articulate what the AI got wrong
- Judges how much effort the correction is worth

**AI System**

- Processes the correction signal and updates its understanding of intent
- Generates an improved output addressing the specific issue
- Logs the correction type as a training signal

**PM Metrics**

- Regeneration frequency: how often users ask for a second attempt
- Correction type distribution: structural, factual, tonal, format
- Correction to acceptance conversion rate

---

## Stage 7. Trust Formation

> "I can rely on this" 😌

**User Thinking**

- Developing a reliable mental model of what the AI does well
- Applying less scrutiny because past experience justifies it
- Factoring the AI into how they plan and approach tasks upfront

**User Action**

- Reuses the product for the same task with less review
- Uses outputs more directly on lower stakes tasks
- Starts thinking about which other tasks are worth trying

**AI System**

- Personalises output style, tone, and detail from accumulated signals
- Reduces clarifying questions as preferences are established
- Proactively surfaces suggestions from learned usage patterns

**PM Metrics**

- Trust proxy: reduction in edit rate over time for the same user
- Feature return rate within 7 days of first successful use
- Review time on output decreasing as tenure increases

---

## Stage 8. Habit Loop

> "This saves me time" 😊

**User Thinking**

- Reaches for the AI automatically for certain task types
- No longer consciously evaluating whether to use it
- Starting to notice tasks not yet tried with AI

**User Action**

- Uses the product repeatedly as a default part of the workflow
- Integrates it into planning from the start, not just as a finish step
- Explores the AI for adjacent tasks beyond the original use case

**AI System**

- Maintains long term memory of preferences, task types, output formats
- Proactively surfaces suggestions at the moment of highest relevance
- Recognises recurring patterns and optimises without being asked

**PM Metrics**

- DAU to WAU ratio: active days per week
- Session frequency and average tasks per session
- Workflow integration depth: starts tasks in the AI versus brings tasks to it

---

## Stage 9. Advocacy

> "Others should use this" 🤩

**User Thinking**

- Has a clear, articulable reason the AI made them better at their job
- Genuine desire to share so colleagues benefit
- May see a competitive advantage in knowing something others do not

**User Action**

- Shares outputs, demos on a real task, recommends in team channels
- Creates or shares prompt templates that worked well
- May propose team or company wide adoption to a manager

**AI System**

- Generates shareable artifacts: formatted outputs, exports, links
- Enables collaboration: shared prompts, team history, multi user sessions
- Surfaces the most compelling output examples to share

**PM Metrics**

- Referral rate: new users from a share or recommendation
- Shared output open rate
- Viral coefficient within organisations
