## 🚀 Josh Talks AI Product Challenge - Data-Driven AI Dataset Collection

This repository contains the solutions and design artifacts focused on two key areas for **Josh Talks AI (Humanness)**: a Vision-Language dataset collection platform (Task 1) and a transcription quality assurance system (Task 2).

***

## 🌄 Task 1: Vision-Language Dataset Collection Platform (Project Drishti)

[cite_start]This project tackles the challenge of building a simple, scalable product (Project Drishti) to collect **culturally rich, location-verified images and descriptions** from villages across India[cite: 45, 46]. [cite_start]The goal is to collect 1,000 images per village across all Indian districts to train and fine-tune Vision-Language (VL) models to be culturally inclusive[cite: 47, 49].

* [cite_start]**Problem:** Today's AI models are "culturally biased" and often fail to recognize Indian contexts (like a Durga Puja pandal)[cite: 160].
* [cite_start]**Design Focus:** Clarity, inclusivity, and **data integrity** for contributors facing low connectivity and varied devices[cite: 51, 55].
* **Key Features:**
    * [cite_start]**Location Verification:** Requires GPS to flag submissions as "Verified Capture" vs. high-risk "Gallery Upload"[cite: 177, 184].
    * [cite_start]**Offline Drafts:** Securely saves verified photos and GPS data for later upload in low-connectivity areas[cite: 190, 191].
    * [cite_start]**Admin Filter + Trust Flags:** Enables internal teams to monitor district coverage and prioritize review based on risk flags (e.g., "Gallery Upload") to catch fraud/spam[cite: 79, 215, 233].

***

## 📈 Task 2: Low-Quality Transcriber Detection System (Project Sentry)

[cite_start]This project focuses on protecting the quality of **Josh Talks AI's** multilingual voice datasets by designing **Project Sentry**, an automated system to identify and flag low-quality transcribers on the *Josh Jobs* platform[cite: 238, 241].

* [cite_start]**Problem:** Transcribers rushing tasks, making minimal effort, or using bots, which degrades data quality and causes financial waste[cite: 125, 126, 239].
* **Analysis:** Identified definitive behavioral patterns using data metrics:
    * **Near-Zero "Thinking Time":** Detecting users who submit instantly after the audio ends, calculated as:
        [cite_start]$$\text{Adjusted Time} = \text{time\_taken\_by\_user} - \text{duration}$$ [cite: 288, 320]
    * [cite_start]**Non-Human Typing Speed:** Detecting scripts/bots that perform edits too quickly for a human, measured via an **Edit Distance / Adjusted Time** heuristic ("Typing Speed" $\text{> 50}$)[cite: 320, 337].
* [cite_start]**Actionable Recommendations (Trust Score System):** An automated Trust Score system is proposed with clear thresholds for warnings and account freezing[cite: 351, 354]:
    * [cite_start]**Flagged Task Penalty:** $-10$ points[cite: 353].
    * [cite_start]**Probation Threshold:** Score $< 50$ (Automated warning)[cite: 355].
    * [cite_start]**Frozen Threshold:** Score $< 20$ (Account blocked)[cite: 358].
