---
layout: default
title: "Horizon Summary: 2026-05-26 (EN)"
date: 2026-05-26
lang: en
---

> From 19 items, 12 important content pieces were selected

---

1. [Using AI to write better code more slowly](#item-1) ⭐️ 7.0/10
2. [Educational Guide to Shamir's Secret Sharing Cryptography](#item-2) ⭐️ 7.0/10
3. [What we lost when we stopped letting kids leave the front yard](#item-3) ⭐️ 7.0/10
4. [Programming Books Declining as Developers Shift to Online Resources](#item-4) ⭐️ 7.0/10
5. [Apple Patches macOS Kernel Vulnerability CVE-2026-28952 Discovered with AI](#item-5) ⭐️ 7.0/10
6. [Armin Ronacher critiques AI-rewritten issue reports in open source](#item-6) ⭐️ 7.0/10
7. [Norway builds sovereign Norwegian-language LLM with Huawei storage](#item-7) ⭐️ 6.0/10
8. [Mullvad rolls out mitigation for VPN exit IP fingerprinting vulnerability](#item-8) ⭐️ 6.0/10
9. [California proposes exempting Linux from age-verification law](#item-9) ⭐️ 6.0/10
10. [Datasette 1.0a30 adds customizable Jump menu with plugin support](#item-10) ⭐️ 6.0/10
11. [datasette-agent 0.1a4 adds AI chat to database jump menu](#item-11) ⭐️ 6.0/10
12. [Developer Recreates 1980s Usborne 'Mad House' Game as Interactive Web Version](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Using AI to write better code more slowly](https://nolanlawson.com/2026/05/25/using-ai-to-write-better-code-more-slowly/) ⭐️ 7.0/10

A discussion exploring how developers can leverage AI tools to improve code quality through iterative refinement and multi-model review processes rather than prioritizing raw speed. The approach involves using different LLM models sequentially—slower, higher-quality models for initial implementation and faster models for specialized review tasks—to catch edge cases and improve overall code reliability. This challenges the common misconception that AI coding tools are primarily meant to produce code quickly, instead demonstrating that thoughtful AI-assisted workflows can enhance code quality and developer productivity when speed is deprioritized. The multi-model review approach represents a practical pattern for organizations seeking to use AI for code review automation and quality assurance without deskilling developers. The workflow described involves using Claude 4.7 Max for slower but higher-quality implementation work, followed by faster models like Codex GPT 5.5 for specialized review that catches corner cases, with iterative refinement loops between models. Developers report that while this process takes longer than writing code by hand, the quality improvements and reduced bugs justify the additional review and iteration time.

hackernews · signa11 · May 25, 23:16 · [Discussion](https://news.ycombinator.com/item?id=48272984)

**Background**: Large Language Models (LLMs) like Claude and GPT have become increasingly capable at code generation, but their outputs vary significantly in quality depending on the model and task complexity. Code review automation using LLMs has emerged as a practical application where multiple models can be combined to provide complementary strengths—some models excel at generating code while others are better at identifying issues or edge cases. Traditional developer workflows prioritize speed, but AI-assisted development is revealing that quality-focused workflows with multiple review passes can produce more reliable code.

<details><summary>References</summary>
<ul>
<li><a href="https://llm-council.dev/integrations/n8n/">A multi - LLM deliberation system for collaborative AI reasoning</a></li>
<li><a href="https://www.ibm.com/think/tutorials/llm-code-review">Perform LLM code review using IBM Bob</a></li>
<li><a href="https://arxiv.org/html/2505.16339v1">Rethinking Code Review Workflows with LLM Assistance: An Empirical Study</a></li>

</ul>
</details>

**Discussion**: Community members largely agree that AI coding tools can produce high-quality code when used thoughtfully, with several developers sharing their own multi-model workflows combining slower, higher-quality models with faster specialized reviewers. However, some commenters note that the iterative review process can actually consume more time than manual coding, particularly when LLM outputs require significant refinement, though they acknowledge the quality benefits justify this investment. There is also appreciation for using AI for code review tasks specifically, as this application is seen as augmenting rather than replacing developer judgment and skills.

**Tags**: `#AI-assisted development`, `#code quality`, `#LLM workflows`, `#developer productivity`, `#code review automation`

---

<a id="item-2"></a>
## [Educational Guide to Shamir's Secret Sharing Cryptography](https://ente.com/blog/how-shamirs-secret-sharing-works/) ⭐️ 7.0/10

Ente published an educational explanation of Shamir's Secret Sharing (SSS), a cryptographic technique developed by Adi Shamir in 1979 that allows secrets to be distributed across multiple parties with threshold-based recovery. The article explains how this polynomial-based method enables a secret to be reconstructed only when a minimum number of share holders cooperate. Shamir's Secret Sharing is fundamental to threshold cryptography and has practical applications in securing sensitive information like DNS root keys and encrypted backups. Understanding this technique is important for security professionals and developers implementing distributed trust systems where no single party should hold complete control over critical secrets. The technique uses polynomial interpolation where a secret is encoded as a constant term in a polynomial, and shares are generated by evaluating the polynomial at different points; any threshold number of shares can reconstruct the original secret through Lagrange interpolation. For large secrets, the approach is typically combined with encryption, and alternative methods like Reed-Solomon codes or PAR2-like systems can be used for payload distribution, though they may sacrifice information-theoretic security compared to pure Shamir sharing.

hackernews · subract · May 25, 22:37 · [Discussion](https://news.ycombinator.com/item?id=48272715)

**Background**: Shamir's Secret Sharing is a cryptographic algorithm that divides a secret into multiple shares distributed among different parties, where the secret cannot be revealed unless a minimum threshold number of parties cooperate. The scheme is based on polynomial mathematics: a secret is embedded as the constant term of a polynomial, and shares are created by evaluating this polynomial at different points. Threshold cryptography, of which SSS is a key example, enables systems where multiple parties must collaborate to perform cryptographic operations, preventing any single entity from having complete control over sensitive information.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Shamir's_secret_sharing">Shamir's secret sharing - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Threshold_cryptosystem">Threshold cryptosystem - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community members highlighted the educational value of the technique, noting it could be taught in secondary schools as an elegant application of polynomials in computer science. Technical discussions compared Shamir's approach with alternative methods like Reed-Solomon codes and PAR2-like systems, with commenters noting trade-offs between information-theoretic security and practical implementation complexity, and discussing how large secrets are typically handled through encryption combined with share distribution.

**Tags**: `#cryptography`, `#secret-sharing`, `#security`, `#polynomial-mathematics`

---

<a id="item-3"></a>
## [What we lost when we stopped letting kids leave the front yard](https://stevemagness.substack.com/p/the-cost-of-safetyism) ⭐️ 7.0/10

An examination of how reduced outdoor freedom for children reflects and reinforces broader losses in community structure, walkability, and intergenerational social bonds in modern suburban life.

hackernews · obscurette · May 25, 14:29 · [Discussion](https://news.ycombinator.com/item?id=48267290)

**Tags**: `#parenting`, `#urban-design`, `#community`, `#social-change`, `#child-development`

---

<a id="item-4"></a>
## [Programming Books Declining as Developers Shift to Online Resources](https://unix.foo/posts/nobody-cracks-open-a-programming-book/) ⭐️ 7.0/10

A discussion on the declining relevance of traditional programming books reveals concrete sales data showing reduced paperback purchases, with O'Reilly author Jon Bodner sharing 13 months of sales figures for "Learning Go" averaging 200-300 copies monthly, down from historical peaks. The debate highlights how search engines and online documentation have fundamentally changed how developers acquire programming knowledge. This trend reflects a significant shift in developer learning culture and has implications for how programming languages are designed and documented. The decline of comprehensive book-based learning has removed constraints on language complexity, allowing languages like C++ to become more feature-rich but harder to master without structured guidance. "Learning Go" has sold approximately 20,000 copies since its 2021 release, with monthly sales fluctuating between 124 and 484 units over the measured period, indicating volatility rather than consistent decline. However, some developers argue that comprehensive books remain valuable for learning language idioms and best practices that cannot be easily acquired through fragmented online searches.

hackernews · zdw · May 25, 23:21 · [Discussion](https://news.ycombinator.com/item?id=48273030)

**Background**: Programming books have traditionally been a primary learning resource for developers, with comprehensive volumes covering language fundamentals, design patterns, and best practices. The rise of the internet, search engines like Google, and community platforms like Stack Overflow have provided alternative, often more immediately accessible sources of programming knowledge. This shift has been particularly pronounced as programming languages have grown more complex, making it impractical for developers to rely solely on memorized knowledge from books.

**Discussion**: Community members present nuanced perspectives: some acknowledge declining book sales but argue that comprehensive books remain essential for learning language idioms and subtle concepts (as exemplified by developers who repeatedly read "Rust for Rustaceans"), while others note that language complexity has increased beyond what traditional books can effectively constrain, and some report mixed experiences with introductory programming books that may lack practical depth. The discussion reflects broader disagreement about whether online resources adequately replace structured book-based learning.

**Tags**: `#programming-education`, `#technical-books`, `#learning-resources`, `#industry-trends`, `#developer-culture`

---

<a id="item-5"></a>
## [Apple Patches macOS Kernel Vulnerability CVE-2026-28952 Discovered with AI](https://support.apple.com/en-us/127115) ⭐️ 7.0/10

Apple released a security patch for CVE-2026-28952, a kernel vulnerability in macOS 26.5 (Tahoe) that was discovered through AI-assisted analysis by Claude and Anthropic Research in collaboration with security researchers at Calif.io. The vulnerability, an integer overflow issue, could allow applications to cause unexpected system termination and affected multiple Apple platforms including iOS 18.7.9, iPadOS 18.7.9, macOS Sequoia 15.7.7, macOS Sonoma 14.8.7, and macOS Tahoe 26.5. This vulnerability affects millions of Apple users across multiple platforms and demonstrates the growing role of AI in security research, raising important questions about vulnerability disclosure practices and the transparency differences between major tech companies. The patch is critical because kernel vulnerabilities can potentially be exploited for privilege escalation and system compromise, making timely updates essential for user security. The vulnerability is specifically an integer overflow addressed through improved input validation in the kernel component. Community members noted that this vulnerability is distinct from recent MIE (Memory Integrity Exploitation) attacks that exploited different kernel bugs, and that similar vulnerabilities affect multiple macOS versions, not just the newest Tahoe release.

hackernews · dragonsenseiguy · May 25, 23:40 · [Discussion](https://news.ycombinator.com/item?id=48273169)

**Background**: Kernel vulnerabilities are security flaws in the operating system's core (ring 0 privilege level) that can be more dangerous than user-space vulnerabilities because they run with the highest system privileges. Integer overflow vulnerabilities occur when arithmetic operations exceed the maximum value a variable can hold, potentially leading to unexpected behavior or memory corruption. AI-assisted vulnerability discovery represents an emerging trend where machine learning models help security researchers identify potential security flaws more efficiently than manual code review alone.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cisa.gov/resources-tools/programs/coordinated-vulnerability-disclosure-program">Coordinated Vulnerability Disclosure Program - CISA</a></li>
<li><a href="https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html">Vulnerability Disclosure - OWASP Cheat Sheet Series</a></li>

</ul>
</details>

**Discussion**: The discussion reveals several key concerns: security researchers at Calif.io clarified that this vulnerability is unrelated to their recent MIE attacks and that their original bugs remain unfixed; community members noted significant transparency differences between Apple and Google's vulnerability disclosure practices, with Google patching 225 internally-found vulnerabilities versus Apple's apparent lack of public disclosure of internal findings; and users raised practical frustration about Apple's update requirements, with one user reporting needing 13.2 GB of free space to update a 64 GB iPhone, which they characterized as poor software development practice.

**Tags**: `#security`, `#vulnerability`, `#macOS`, `#kernel`, `#AI-assisted-security`

---

<a id="item-6"></a>
## [Armin Ronacher critiques AI-rewritten issue reports in open source](https://simonwillison.net/2026/May/24/armin-ronacher/#atom-everything) ⭐️ 7.0/10

Armin Ronacher, a prominent open-source maintainer, has publicly criticized the practice of submitting AI-rewritten issue reports, arguing that they create confusion and poor debugging outcomes. He advocates for issue reports to be limited to simple, human-observed problem statements following a four-point format: what command was run, what was expected, what actually happened, and the exact error or log output. This critique addresses a growing pain point in open-source maintenance as AI tools become more prevalent in software development workflows. Poor-quality, AI-generated issue reports waste maintainers' time with inaccurate root cause analysis, fake minimal reproductions, and overconfident but incorrect suggestions, directly impacting the efficiency and sustainability of open-source projects. Ronacher describes the problem as AI-generated content that has been "thrown into a clanker" (reworded by language models), resulting in conclusions that are typically inaccurate but presented with high confidence. The issues often contain guesswork about root causes, fake minimal reproductions, incorrect implementation strategies, and irrelevant error class lists that obscure the actual observed problem.

rss · Simon Willison · May 24, 18:46

**Background**: Open-source maintainers rely on well-written issue reports to understand and fix bugs efficiently. Issue reports typically describe what a user did, what they expected to happen, and what actually occurred. As AI tools like large language models have become more accessible, some users have begun using them to rewrite or enhance their issue reports, sometimes with unintended negative consequences for clarity and accuracy.

**Tags**: `#open-source`, `#issue-reporting`, `#AI-generated-content`, `#software-maintenance`, `#best-practices`

---

<a id="item-7"></a>
## [Norway builds sovereign Norwegian-language LLM with Huawei storage](https://www.blocksandfiles.com/flash/2026/05/22/norways-2-petabytes-of-huawei-flash-storage-and-llm-training/5244910) ⭐️ 6.0/10

Norway's National Library is developing a sovereign large language model (LLM) trained specifically on Norwegian-language content, utilizing 2 petabytes of Huawei flash storage and an HPE Cray supercomputer called Olivia with 448 GPUs and 64,512 CPU cores. The project was presented by Marius Husnes, Head of IT Platform at the National Library, at Huawei's ID Forum 2026 in Paris. The project reflects growing concerns about language-specific AI capabilities and cultural preservation, as globally-trained English-centric LLMs may lack knowledge of local history, news, and culture documented in minority languages. This initiative highlights the emerging trend of sovereign AI infrastructure as countries seek to develop independent language models rather than relying solely on commercial providers. The Olivia supercomputer system represents a mid-range computing platform compared to leading global LLM training infrastructure, which has raised questions in the technical community about whether the hardware is sufficient for training a fully-fledged LLM from scratch versus using more efficient approaches like fine-tuning existing open-source models. The National Library's existing text search infrastructure is noted as having one of the best user interfaces for searching through massive text collections.

hackernews · rbanffy · May 25, 19:37 · [Discussion](https://news.ycombinator.com/item?id=48270770)

**Background**: Large language models (LLMs) are AI systems trained on vast amounts of text data to understand and generate human language. Most commercially dominant LLMs like GPT-4 are trained primarily on English-language data and may have limited knowledge of non-English languages and cultures. Sovereign AI refers to a country's ability to develop and control its own AI systems independently, rather than relying on foreign commercial providers. The HPE Cray Supercomputing EX is a high-performance computing platform designed for intensive computational tasks like machine learning model training.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techpolicy.press/sovereignty-myth-making-in-the-ai-race/">'Sovereignty' Myth-Making in the AI Race | TechPolicy.Press</a></li>
<li><a href="https://northwiseproject.com/sovereign-ai-infrastructure/">AMD Sovereign AI Infrastructure : AMD and National AI Systems</a></li>

</ul>
</details>

**Discussion**: Community discussion reveals significant skepticism about the project's feasibility and goals. A key concern is whether the Olivia supercomputer's specifications (448 GPUs and 64,512 CPU cores) are sufficient for training a fully-fledged LLM from scratch, with some commenters suggesting that fine-tuning existing open-source models via LoRA would be more efficient and questioning whether the project's stated ambitions are realistic. However, others acknowledge the National Library's strong existing infrastructure for text search and retrieval, and debate whether the assertion about English-centric LLMs lacking knowledge of Norwegian culture is accurate given that major models train on diverse multilingual data.

**Tags**: `#LLM`, `#sovereign-AI`, `#infrastructure`, `#language-models`, `#geopolitics`

---

<a id="item-8"></a>
## [Mullvad rolls out mitigation for VPN exit IP fingerprinting vulnerability](https://mullvad.net/en/help/exit-ip-vpn-servers-mitigation-rollout) ⭐️ 6.0/10

Mullvad has begun rolling out a mitigation to address an exit IP fingerprinting vulnerability that allows websites to probabilistically correlate user activity across different VPN servers. The company discovered that each VPN server assigns users one of several exit IP addresses from a shared pool, enabling attackers to track users as they switch between servers. This vulnerability undermines a core privacy promise of VPN services—the ability to hide user activity and prevent tracking across different servers. The swift mitigation rollout demonstrates Mullvad's commitment to security and has impressed users accustomed to slower responses from larger tech companies. The vulnerability is classified as minor and affects the ability to correlate user activity across VPN servers through exit IP analysis. Mullvad Browser users with built-in proxies and DAITA (Defend Against Targeted Ads) are noted as having additional protections against fingerprinting attacks.

hackernews · Cider9986 · May 25, 17:45 · [Discussion](https://news.ycombinator.com/item?id=48269580)

**Background**: VPN fingerprinting is a technique where websites identify and track users by analyzing unique characteristics of their connection or device, even when using a VPN. Exit IP fingerprinting specifically exploits the fact that VPN servers distribute users across a limited pool of exit IP addresses; by observing which exit IPs are used together, attackers can probabilistically link a user's activity across different VPN servers. This differs from traditional tracking methods and represents a more subtle privacy threat that many users may not be aware of.

<details><summary>References</summary>
<ul>
<li><a href="https://mullvad.net/en/blog/2026/5/20/exit-ip-fingerprinting-between-vpn-servers">Exit IP fingerprinting between VPN servers - mullvad.net</a></li>
<li><a href="https://cyberinsider.com/mullvad-confirms-vpn-fingerprinting-flaw-says-fix-is-on-the-way/">Mullvad confirms VPN fingerprinting flaw, says fix is on the way</a></li>
<li><a href="https://www.techradar.com/vpn/vpn-services/mullvad-to-patch-vpn-fingerprinting-issue-to-stop-your-activity-from-being-tracked-across-servers">Mullvad to patch VPN fingerprinting issue to stop your ...</a></li>

</ul>
</details>

**Discussion**: Community members praised Mullvad's unusually prompt response to the vulnerability, with one user noting surprise at such swift action in the modern tech industry. Discussion highlighted complementary privacy solutions like Mullvad Browser's Random mode feature and DAITA, while others suggested standardized browser fingerprinting spoofing across all users rather than random spoofing. Some users noted geographic limitations, with Asian servers being excluded from the initial rollout.

**Tags**: `#VPN`, `#privacy`, `#security`, `#fingerprinting`, `#mitigation`

---

<a id="item-9"></a>
## [California proposes exempting Linux from age-verification law](https://www.tomshardware.com/software/linux/california-moves-to-exempt-linux-from-its-upcoming-age-verification-law-after-backlash-over-forcing-operating-systems-to-collect-users-ages-amendment-proposed-by-the-same-lawmaker-who-wrote-the-original-law) ⭐️ 6.0/10

California is moving to exempt Linux from its age-verification law after significant backlash from the open-source community over requirements that operating systems collect user age data. The exemption amendment has been proposed by the same lawmaker who authored the original legislation. This exemption protects open-source operating systems from compliance burdens that could have stifled development and innovation in the Linux ecosystem. The broader issue highlights how technology regulation can inadvertently impose impractical requirements on distributed, community-driven projects that lack centralized enforcement mechanisms. The original law would have required operating systems themselves to implement age verification and collect user age data, which is technically impractical for Linux given its decentralized development model and the fact that age verification is typically a responsibility of content platforms rather than OS vendors. The exemption suggests recognition that age verification requirements are better suited to web browsers and content platforms than to the operating system layer.

hackernews · rbanffy · May 25, 18:19 · [Discussion](https://news.ycombinator.com/item?id=48269961)

**Background**: Age-verification laws are regulations designed to restrict minors' access to age-restricted content online, such as adult material or gambling sites. California's legislation attempted to mandate that operating systems implement these verification mechanisms, which would affect how users interact with their computers at a fundamental level. Linux is a free, open-source operating system maintained by a distributed community of developers worldwide, making it difficult to impose centralized compliance requirements on the project.

**Discussion**: Community comments reveal significant confusion about the law's actual scope and requirements, with some commenters suggesting alternative approaches like browser-level parental controls rather than OS-level mandates. Critics argue the law reflects regulatory overreach and a failure of public institutions to regulate companies directly, instead burdening consumers and open-source developers. Some commenters speculate the exemption may be strategically designed to prevent Linux developers from having legal standing to challenge the law on First Amendment grounds.

**Tags**: `#policy`, `#open-source`, `#regulation`, `#privacy`, `#linux`

---

<a id="item-10"></a>
## [Datasette 1.0a30 adds customizable Jump menu with plugin support](https://simonwillison.net/2026/May/24/datasette/#atom-everything) ⭐️ 6.0/10

Datasette 1.0a30 introduces a new customizable "Jump to..." menu accessible by pressing the forward slash key, which allows users to quickly navigate to databases, tables, and debug options. The release also adds a new jump_items_sql() plugin hook that enables plugins to extend the searchable items in this navigation menu. This feature improves user experience by providing a fast, keyboard-driven way to navigate complex Datasette instances with multiple databases and tables. The extensible plugin hook architecture allows the community to build custom navigation extensions, making Datasette more adaptable to different workflows and use cases. The Jump menu is triggered by pressing the forward slash key and filters results as users type, displaying matching databases, tables, and debug options. This is an alpha release (1.0a30), meaning it is still in pre-release development and may undergo further changes before the stable 1.0 version.

rss · Simon Willison · May 24, 23:52

**Background**: Datasette is an open-source multi-tool for exploring and publishing data, allowing users to import data from CSVs, JSON, database connections, and other sources. The tool automatically identifies patterns in data and helps users share findings with colleagues. Plugin hooks are a software architecture pattern that allows third-party developers to extend application functionality by registering callbacks that execute at specific points in the application's workflow.

<details><summary>References</summary>
<ul>
<li><a href="https://datasette.io/">Datasette : An open source multi- tool for exploring and publishing data</a></li>
<li><a href="https://github.com/simonw/datasette">GitHub - simonw/ datasette : An open source multi- tool for exploring...</a></li>

</ul>
</details>

**Tags**: `#datasette`, `#database-tools`, `#plugin-architecture`, `#ui-ux`, `#python`

---

<a id="item-11"></a>
## [datasette-agent 0.1a4 adds AI chat to database jump menu](https://simonwillison.net/2026/May/24/datasette-agent/#atom-everything) ⭐️ 6.0/10

datasette-agent 0.1a4 now integrates with Datasette 1.0a30's new makeJumpSections() JavaScript plugin hook to display an AI chat interface in the Jump to menu (accessed via the / key), allowing users to start natural language database queries directly from the menu. This integration improves the user experience for database exploration by making AI-powered natural language queries more discoverable and accessible within Datasette's core navigation interface, potentially lowering the barrier for non-technical users to query databases. The feature is demonstrated on agent.datasette.io where users can sign in via GitHub; the implementation leverages the new makeJumpSections() hook introduced in Datasette 1.0a30 released on May 24, 2026.

rss · Simon Willison · May 24, 23:19

**Background**: Datasette is an open-source multi-tool for exploring and publishing data from various sources including CSVs, JSON, and database connections. datasette-agent is an AI-powered extension that enables natural language queries against databases. JavaScript plugin hooks in Datasette allow developers to extend the application's functionality by injecting custom UI elements and behavior into specific parts of the interface.

<details><summary>References</summary>
<ul>
<li><a href="https://datasette.io/">Datasette : An open source multi- tool for exploring and publishing data</a></li>
<li><a href="https://github.com/simonw/datasette">GitHub - simonw/ datasette : An open source multi- tool for exploring...</a></li>

</ul>
</details>

**Tags**: `#datasette`, `#ai-agents`, `#javascript-plugins`, `#database-tools`, `#alpha-release`

---

<a id="item-12"></a>
## [Developer Recreates 1980s Usborne 'Mad House' Game as Interactive Web Version](https://simonwillison.net/2026/May/24/usborne-mad-house/#atom-everything) ⭐️ 6.0/10

A developer has recreated the 1983 Usborne computer game 'Mad House' from the book 'Creepy Computer Games' as an interactive JavaScript and HTML web application. The recreation was built by feeding the original PDF into Claude AI with a prompt to build a vanilla JavaScript artifact that matches the original game while maintaining a retro aesthetic and mobile-friendly design. This project demonstrates practical AI-assisted web development for preserving retro computing history and making vintage games accessible to modern audiences without requiring original hardware. It showcases how freely available vintage computer book PDFs and modern AI tools can be combined to revive nostalgic software experiences. The recreation uses a retro green-on-black terminal-style interface with ASCII art corridors, matching the original game's aesthetic from the 1980s Commodore 64 era. The game includes the original controls (X and C for near doors, N and M for far doors) and features like footstep counters and door tracking, all built with vanilla JavaScript without additional frameworks.

rss · Simon Willison · May 24, 17:14

**Background**: Usborne was a UK publisher known for producing beautifully illustrated computer books in the 1980s that contained code projects readers could type into their own machines, such as Commodore 64 computers. The publisher recently made PDFs of these classic books freely available online, allowing people to access the same programming exercises and games they may have used decades ago. 'Mad House' was a game from the 1983 book 'Creepy Computer Games' that challenged players to navigate through corridors and manage doors to survive a haunted house scenario.

**Tags**: `#retro-computing`, `#AI-assisted-development`, `#nostalgia`, `#web-development`, `#game-recreation`

---