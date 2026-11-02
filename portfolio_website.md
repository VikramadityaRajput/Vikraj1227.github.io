---
name: build-cs-portfolio
description: Generates and updates a high-signal computer science student portfolio website focusing on quality projects, clear architecture, and recruiter-friendly UX.
---

## Context
The user is Vikramaditya, an undergraduate Computer Science and Statistics student at the University of Illinois Urbana-Champaign (UIUC). The goal of this portfolio is to secure Summer 2027 Software Engineering and Quantitative Development internships. 

## Instructions
1. **Scaffold the Foundation:** Set up a clean, responsive web project. Prioritize semantic HTML and CSS over heavy JavaScript frameworks unless dynamic routing is strictly necessary.
2. **Build the Hero Section:** Include a concise, professional summary highlighting the user's focus on backend systems, data analysis, and quantitative development. Prominently display working links to GitHub, LinkedIn, and a downloadable Resume PDF.
3. **Structure the Experience Section:** Highlight professional experience first. Emphasize the Summer 2026 Software Engineering Internship at Tradegrub, detailing the development of backend scheduling APIs, Model Context Protocol servers, and PostgreSQL data layers using Python, FastAPI, and GraphQL.
4. **Structure the Projects Section:** Implement the "Student Proof Ladder" by focusing on a few deep, highly technical projects:
    *   **Limit Order Book Engine:** Highlight the single-threaded C++20 LOB Reconstruction Engine, mentioning the parsing of Nasdaq ITCH 5.0 binary feeds and the 1.5M messages/sec throughput at 55µs p99 latency.
    *   **Eco Illini Supermileage:** Highlight the Data Analysis Lead role, detailing the Extended Kalman Filters and Particle Swarm Optimization scripts built in MATLAB for vehicle state estimation.
5. **Optimize for Speed and Scanning:** Ensure the layout utilizes clear visual hierarchy. Use bullet points for technical achievements and avoid dense walls of text. 

## Best Practices
*   **Progressive Enhancement:** Do not use polyfills. Rely on progressive enhancement so that the site remains functional even on older browsers.
*   **Design Tokens & Dark Mode:** Implement dark mode strictly using CSS variables and the `light-dark()` function. Base primitives (`--p-*`) should map to semantic tokens (`--s-*`). The CSS must default to the system preference, ensuring the site themes correctly even if JavaScript fails.
*   **Zero Fluff:** Do not include a "skills cloud" of 20+ programming languages, hobby projects, or class assignments. Let the C++, Python, and MATLAB projects speak for themselves.
*   **Deployment Readiness:** Ensure the final build does not contain hardcoded `localhost` URLs or temporary debug files, making it immediately ready for static deployment (e.g., GitHub Pages, Cloudflare Pages, or Hostinger).