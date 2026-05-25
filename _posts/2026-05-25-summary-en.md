---
layout: default
title: "Horizon Summary: 2026-05-25 (EN)"
date: 2026-05-25
lang: en
---

> From 15 items, 11 important content pieces were selected

---

1. [Mullvad rolls out mitigation for VPN exit IP fingerprinting vulnerability](#item-1) ⭐️ 7.0/10
2. [C compiler portability: managing extensions and cross-platform compatibility](#item-2) ⭐️ 7.0/10
3. [IBM Spins Off Quantum Computing as Independent Foundry with $2B CHIPS Act Funding](#item-3) ⭐️ 7.0/10
4. [Audiomass: Free, Open-Source Web-Based Multitrack Audio Editor](#item-4) ⭐️ 7.0/10
5. [DeepSeek Reasonix: Native coding agent with prompt caching and low costs](#item-5) ⭐️ 7.0/10
6. [Armin Ronacher Critiques AI-Generated Issue Reports in Open Source](#item-6) ⭐️ 7.0/10
7. [Magnifica Humanitas](#item-7) ⭐️ 6.0/10
8. [California proposes exempting Linux from age-verification law](#item-8) ⭐️ 6.0/10
9. [Netherlands Seizes 800 Servers, Arrests 2 for Cyberattack Infrastructure](#item-9) ⭐️ 6.0/10
10. [Datasette 1.0a30 adds customizable Jump menu with plugin extensibility](#item-10) ⭐️ 6.0/10
11. [Developer Recreates 1980s Usborne 'Mad House' Game Using Claude AI](#item-11) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Mullvad rolls out mitigation for VPN exit IP fingerprinting vulnerability](https://mullvad.net/en/help/exit-ip-vpn-servers-mitigation-rollout) ⭐️ 7.0/10

Mullvad has announced a mitigation rollout addressing vulnerabilities in its VPN exit IP infrastructure that could enable user fingerprinting and identification through correlation attacks. The vulnerability allows attackers to link different online activities to the same user by tracking consistent exit IP patterns across multiple sessions and services. This vulnerability undermines a core promise of VPN services—protecting user privacy and preventing identification—by enabling correlation attacks that can link browsing activities across different platforms without exposing the user's real IP address. The issue has broader implications for VPN security practices and has drawn attention from policymakers, including Senator Wyden's recent congressional warnings about VPN infrastructure vulnerabilities. Exit IP fingerprinting does not directly expose a user's real identity or IP address, but when combined with IP logs, account activity records, moderation data, or breached datasets, it can enable high-confidence correlation attacks to identify users. The vulnerability affects VPN users who rely on consistent exit IPs, and mitigation requires changes to how VPN providers manage their exit server infrastructure.

hackernews · Cider9986 · May 25, 17:45 · [Discussion](https://news.ycombinator.com/item?id=48269580)

**Background**: VPN (Virtual Private Network) services encrypt user traffic and route it through remote servers to mask the user's real IP address and location. Exit IP fingerprinting is a technique where attackers correlate a user's consistent VPN exit IP address across multiple services or sessions to build a behavioral profile and link different online activities together. Browser and device fingerprinting are related techniques that identify users based on unique combinations of device characteristics, browser settings, and behavioral patterns—methods that VPNs alone cannot fully prevent. These vulnerabilities highlight that VPNs protect against IP-based tracking but are insufficient against more sophisticated identification methods.

<details><summary>References</summary>
<ul>
<li><a href="https://cyberinsider.com/mullvad-vpn-exit-ip-patterns-could-enable-user-fingerprinting/">Mullvad VPN exit IP patterns could enable user fingerprinting</a></li>
<li><a href="https://factually.co/fact-checks/technology/how-correlation-attacks-link-vpn-exit-traffic-to-users-4da4df">How do correlation attacks link VPN exit traffic to cl...</a></li>
<li><a href="https://hackaday.com/2025/11/19/browser-fingerprinting-and-why-vpns-wont-make-you-anonymous/">Browser Fingerprinting And Why VPNs Won’t Make You Anonymous | Hackaday</a></li>

</ul>
</details>

**Discussion**: Community discussion highlights concerns about the broader scope of fingerprinting beyond exit IPs, with commenters suggesting that browser and device fingerprinting standardization (rather than randomization) could improve privacy without sacrificing functionality. Questions were raised about whether this vulnerability is related to Senator Wyden's recent congressional warnings about VPN infrastructure, and whether other VPN providers are addressing similar issues. Some commenters also inquired about the business relationships between VPN providers and retail ISPs for exit point provisioning.

**Tags**: `#VPN security`, `#privacy`, `#fingerprinting mitigation`, `#infrastructure`

---

<a id="item-2"></a>
## [C compiler portability: managing extensions and cross-platform compatibility](https://lemon.rip/w/6-c-extensions-compilers/) ⭐️ 7.0/10

An article explores practical strategies for writing C code that compiles and runs across different compilers and platforms, addressing the challenge of non-standard compiler extensions and portability issues that plague real-world C projects. The discussion highlights common patterns like conditional compilation checks for compiler-specific features (e.g., __attribute__) and real-world experiences from compiler developers and maintainers. C code portability is a critical pain point for developers working across multiple platforms and compiler toolchains; poor portability practices lead to code that only works reliably on the original developer's machine, limiting adoption and maintenance. Understanding how to properly handle compiler extensions and non-standard features is essential for writing robust, maintainable C libraries and applications that work in diverse environments. The article and community discussion highlight that many C projects rely on compiler-specific features like GCC's __attribute__ without properly checking if the attribute itself is already defined, and that alternative compilers (like TinyCC or indie compilers) often struggle to compile real-world code because they don't pretend to be __GNUC__. Best practices include using more fine-grained feature detection (checking for specific attribute support rather than just compiler identity) and learning from projects like slimcc that have developed platform-specific header hacks to improve compatibility.

hackernews · xngbuilds · May 25, 14:15 · [Discussion](https://news.ycombinator.com/item?id=48267126)

**Background**: C is known for portability across different hardware platforms and operating systems, but this reputation is often challenged in practice because many C projects rely on non-standard compiler extensions. Non-standard extensions are language features added by specific compilers (like GCC's __attribute__ for function/variable attributes, or Apple's Blocks for closures) that are not part of the ISO C standard. When code uses these extensions without proper conditional compilation guards, it fails to compile on other compilers that don't support them, creating a "works on my machine" problem where code written by Linux developers using GCC may break on Windows or FreeBSD systems.

<details><summary>References</summary>
<ul>
<li><a href="https://gcc.gnu.org/onlinedocs/gcc/C-Extensions.html">C Extensions (Using the GNU Compiler Collection (GCC))</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blocks_(C_language_extension)">Blocks (C language extension) - Wikipedia</a></li>
<li><a href="https://www.sanfoundry.com/c-tutorials-concept-portability-context-programs/">What is Portability in C Programming? - Sanfoundry</a></li>

</ul>
</details>

**Discussion**: The discussion reveals strong consensus on the real-world severity of portability issues, with experienced developers like Walter Bright (creator of the D language) sharing that even implementing a C compiler within another language (ImportC in D) required extensive workarounds for non-standard header quirks. Contributors suggest that better practices involve checking for specific feature support (like __GLIBC_COMPILER_SUPPORTS_ATTRIBUTES__) rather than just compiler identity, and point to projects like slimcc as examples of how indie compilers can document and share solutions for handling platform-specific compatibility challenges.

**Tags**: `#C-programming`, `#compiler-compatibility`, `#portability`, `#systems-programming`, `#best-practices`

---

<a id="item-3"></a>
## [IBM Spins Off Quantum Computing as Independent Foundry with $2B CHIPS Act Funding](https://futurumgroup.com/insights/2-billion-chips-act-investment-in-quantum-bets-on-ibms-300mm-superconducting-silicon/) ⭐️ 7.0/10

IBM has spun off its quantum computing division as a standalone, pure-play foundry company with $2 billion in CHIPS Act funding, separating its speculative quantum ventures from its legacy consulting and enterprise services business. This strategic move positions the new entity to serve as shared infrastructure for other quantum hardware companies, rather than remaining captive to IBM's traditional business model. This spinoff signals a critical recognition that speculative quantum computing ventures require different management structures and capital strategies than IBM's legacy consulting business, potentially accelerating quantum technology commercialization by enabling multiple hardware companies to access shared fabrication resources. The move also reflects broader industry trends toward separating emerging technology bets from mature business units to avoid the fate of failed initiatives like IBM Watson. The foundry model is significant because it allows multiple quantum hardware companies to utilize shared fabrication infrastructure rather than each maintaining separate research cleanrooms, improving capital efficiency and scalability. The spinoff operates on 300mm superconducting silicon technology, though the community notes that alternative approaches like trapped-ion quantum systems exist with different trade-offs in stability windows, accuracy, and operating temperatures.

hackernews · rbanffy · May 25, 09:43 · [Discussion](https://news.ycombinator.com/item?id=48265056)

**Background**: A quantum chip foundry is a specialized semiconductor manufacturing facility designed to produce quantum processors at scale, similar to how traditional semiconductor foundries manufacture conventional chips for multiple customers. The CHIPS Act is a U.S. government initiative providing direct funding and loans to semiconductor manufacturers to restore American leadership in chip production, with major recipients including Intel ($8.5 billion), TSMC ($6.6 billion), and Samsung ($6.4 billion). IBM's previous experience with Watson—an AI system heavily promoted by management despite limited real-world adoption—demonstrated the risks of keeping speculative technology ventures within traditional corporate structures focused on consulting and cost-cutting.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bu.edu/eng/2025/07/14/first-electronic-photonic-quantum-chip-created-in-commercial-foundry/">First Electronic–Photonic Quantum Chip Created in Commercial Foundry | College of Engineering</a></li>
<li><a href="https://www.bakertilly.com/insights/notice-of-funding-chips-act">Notice of funding for the CHIPS act program | Baker Tilly</a></li>
<li><a href="https://www.theverge.com/24166234/chips-act-funding-semiconductor-companies">Where the CHIPS Act money has gone | The Verge</a></li>

</ul>
</details>

**Discussion**: Community members largely support the spinoff as a necessary separation of speculative growth ventures from IBM's traditional consulting-focused business model, with commenters noting that IBM's historical pattern of forcing technology adoption through bundled deals undermined initiatives like Watson. However, some critics argue the article presents a pro-IBM perspective and overlooks alternative quantum approaches like trapped-ion systems that may offer superior stability and accuracy; others emphasize that the real strategic value lies in the foundry's ability to serve as shared infrastructure for multiple quantum hardware companies rather than the $2 billion funding amount itself.

**Tags**: `#quantum-computing`, `#IBM`, `#corporate-strategy`, `#semiconductor-foundry`, `#emerging-technology`

---

<a id="item-4"></a>
## [Audiomass: Free, Open-Source Web-Based Multitrack Audio Editor](https://audiomass.co/?multitrack=1) ⭐️ 7.0/10

Audiomass is a newly showcased free, open-source multitrack audio editor that runs entirely in the web browser with Progressive Web App (PWA) support for offline functionality. The tool features an intuitive user interface and allows users to work with multiple audio tracks simultaneously without requiring internet connectivity once loaded. This project addresses a significant gap in accessible audio editing tools by providing a free, browser-based alternative to expensive desktop software like Adobe Audition, while the PWA offline capability makes it uniquely practical for users without reliable internet access. The open-source nature enables community contributions and customization, potentially inspiring collaborative features like cloud-based track sharing and multi-user jamming workflows. Audiomass leverages the Web Audio API for audio processing and implements PWA technology with service workers to enable offline functionality, allowing users to store the application locally and use it without internet connectivity. The codebase demonstrates classical JavaScript patterns with safety closures and sequential variable declarations, reflecting a deliberate architectural approach rather than modern framework-heavy development.

hackernews · pantelisk · May 24, 15:25 · [Discussion](https://news.ycombinator.com/item?id=48258015)

**Background**: Progressive Web Apps (PWAs) are web applications that use modern web technologies to provide app-like experiences, including the ability to work offline through service workers and local caching. The Web Audio API is a browser standard that enables developers to process and synthesize audio directly in web applications, making it possible to build sophisticated audio editing tools without requiring desktop software. Multitrack audio editing refers to the ability to work with multiple independent audio streams simultaneously, a fundamental feature in music production and audio post-production workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.google.com/codelabs/pwa-training/pwa03--going-offline">Progressive Web Apps : Going Offline</a></li>
<li><a href="https://github.com/naomiaro/waveform-playlist">GitHub - naomiaro/waveform-playlist: Multitrack Web Audio editor and player with canvas waveform preview. Set cues, fades and shift multiple tracks in time. Record audio tracks or provide audio annotations. Export your mix to AudioBuffer or WAV! Add effects from Tone.js. Project inspired by Audacity. · GitHub</a></li>
<li><a href="https://project-awesome.org/notthetup/awesome-webaudio">Awesome WebAudio | Curated list of awesome lists | Project-Awesome.org</a></li>

</ul>
</details>

**Discussion**: Community response has been overwhelmingly positive, with users praising the intuitive UX design and appreciating the offline PWA capability as a transformative feature that embodies the web platform's potential. Several commenters expressed interest in collaborative extensions, such as cloud-based track sharing and version control for multi-user jamming sessions, while others highlighted the tool's practical value as a lightweight, free alternative to commercial audio editors that respects user privacy.

**Tags**: `#web-audio`, `#open-source`, `#PWA`, `#audio-editing`, `#developer-tools`

---

<a id="item-5"></a>
## [DeepSeek Reasonix: Native coding agent with prompt caching and low costs](https://esengine.github.io/DeepSeek-Reasonix/) ⭐️ 7.0/10

DeepSeek Reasonix is a native coding agent that leverages DeepSeek's prompt caching feature and low-cost API pricing to provide an efficient alternative for code generation tasks. The agent is designed to take advantage of DeepSeek's context caching capability, which reuses repeated prompt prefixes across requests to significantly reduce input token costs. This development is significant because it demonstrates how to build cost-effective AI-assisted coding solutions by combining DeepSeek's affordable pricing with intelligent caching strategies, making advanced code generation accessible to developers and organizations with tighter budgets. The approach addresses a key pain point in AI-assisted development—reducing operational costs while maintaining code quality—which could accelerate adoption of coding agents across different project scales. The implementation leverages DeepSeek's context caching API, where cached tokens are charged at $0.014 per million tokens compared to standard input token rates, and the API provides prompt_cache_hit_tokens and prompt_cache_miss_tokens fields to monitor cache performance. Community feedback indicates that effective caching can result in dramatic cost reductions—one user reported caching 39.1 million tokens while only incurring costs for 1.7 million cache-miss tokens—though some users note that the website's presentation and mobile responsiveness could be improved.

hackernews · Alifatisk · May 24, 13:02 · [Discussion](https://news.ycombinator.com/item?id=48256953)

**Background**: Coding agents are specialized AI assistants designed to help developers write, debug, and optimize code by automating routine coding tasks. Prompt caching is a technique where the API stores frequently-used prompt prefixes (such as system prompts or code examples) and reuses them across multiple requests, reducing both latency and token costs. DeepSeek is a cost-competitive AI model provider that has recently made price discounts permanent, making it an attractive option for budget-conscious development teams.

<details><summary>References</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/guides/kv_cache">Context Caching | DeepSeek API Docs</a></li>
<li><a href="https://api-docs.deepseek.com/news/news0802">DeepSeek API introduces Context Caching on Disk, cutting prices by an order of magnitude | DeepSeek API Docs</a></li>
<li><a href="https://github.com/resources/articles/what-are-ai-agents">What are AI agents ? · GitHub</a></li>

</ul>
</details>

**Discussion**: Community discussion reveals mixed sentiment: some users appreciate the cost optimization and report successful caching implementations, while others criticize the website's design and user experience, noting poor mobile responsiveness and unnecessary animations that degrade usability. Technical experts debate the merits of always using caching versus allowing models to break prefix caches when it produces better results, with experienced developers suggesting that caching decisions should be based on empirical testing rather than assumptions.

**Tags**: `#AI/ML`, `#coding-agents`, `#cost-optimization`, `#prompt-caching`, `#deepseek`

---

<a id="item-6"></a>
## [Armin Ronacher Critiques AI-Generated Issue Reports in Open Source](https://simonwillison.net/2026/May/24/armin-ronacher/#atom-everything) ⭐️ 7.0/10

Armin Ronacher, a prominent open-source developer, has publicly criticized the growing problem of AI-generated issue reports submitted to open-source projects, arguing that they are often inaccurate, verbose, and unhelpful. He advocates for a simple four-step format where issue reporters describe only what they actually observed: the command they ran, what they expected, what happened instead, and the exact error or log output. This critique addresses a significant and growing pain point for open-source maintainers who are increasingly burdened with low-quality, AI-generated issue reports that waste their time and distract from genuine bugs. The problem directly impacts the sustainability and quality of open-source software maintenance, as maintainers must spend effort filtering noise rather than solving real problems. Ronacher identifies specific problems with AI-generated reports: they are often reworded by language models in ways that introduce inaccuracy, contain overconfident but incorrect conclusions about root causes, include fake minimal reproductions, suggest irrelevant implementation strategies, and list error classes that may not be relevant. His proposed four-step format strips away all interpretation and focuses purely on observable facts that the human reporter directly experienced.

rss · Simon Willison · May 24, 18:46

**Background**: Open-source software projects rely on community-submitted issue reports to identify and fix bugs. Traditionally, these reports were written by humans who directly experienced problems and could provide context and observations. With the rise of AI language models and coding agents, some users have begun using AI tools to generate or rewrite issue reports, sometimes without fully understanding the underlying problem or verifying the AI's output for accuracy.

**Tags**: `#open-source`, `#issue-reporting`, `#AI-generated-content`, `#software-maintenance`, `#community-standards`

---

<a id="item-7"></a>
## [Magnifica Humanitas](https://www.vatican.va/content/leo-xiv/en/encyclicals/documents/20260515-magnifica-humanitas.html) ⭐️ 6.0/10

A papal encyclical addressing technology's impact on humanity, exploring themes of algorithmic transparency, power concentration, and the ethical responsibilities of technology builders.

hackernews · theletterf · May 25, 10:11 · [Discussion](https://news.ycombinator.com/item?id=48265206)

**Tags**: `#technology-ethics`, `#AI-governance`, `#algorithmic-accountability`, `#philosophy`

---

<a id="item-8"></a>
## [California proposes exempting Linux from age-verification law](https://www.tomshardware.com/software/linux/california-moves-to-exempt-linux-from-its-upcoming-age-verification-law-after-backlash-over-forcing-operating-systems-to-collect-users-ages-amendment-proposed-by-the-same-lawmaker-who-wrote-the-original-law) ⭐️ 6.0/10

California is moving to exempt Linux operating systems from its age-verification law after significant industry backlash over the impracticality of requiring operating systems to collect user age data. The amendment has been proposed by the same lawmaker who authored the original legislation. This regulatory shift highlights the tension between child safety legislation and technical feasibility, affecting how operating systems and software platforms must handle age verification going forward. The exemption could set a precedent for how California and other jurisdictions approach technology regulation, balancing protective intent with practical implementation constraints. The original law would have required operating systems themselves to implement age verification mechanisms, which is technically problematic because operating systems operate at a foundational level and do not inherently know user identity or age. Linux, being open-source and community-maintained, presented particular challenges for compliance with such mandates.

hackernews · rbanffy · May 25, 18:19 · [Discussion](https://news.ycombinator.com/item?id=48269961)

**Background**: Age-verification laws aim to prevent minors from accessing age-restricted content online. California's legislation attempted to address this by mandating that operating systems implement verification mechanisms, but this approach conflates the role of operating systems (which provide the computational platform) with content platforms (which control access to specific services). The distinction is important because operating systems like Linux, Windows, and macOS are foundational software that users interact with before accessing any specific online services.

**Discussion**: Community commenters raised several key concerns: some argued that age verification should be implemented at the browser level rather than the OS level, as this would be more practical and require minimal effort from browser vendors; others questioned the legislative process itself, asking whether California tech companies were consulted; and several noted that such mandates ultimately burden consumers and parents rather than addressing the root issue, which requires parental oversight. There was also skepticism about whether OS-level verification could be effectively circumvented anyway.

**Tags**: `#policy`, `#linux`, `#age-verification`, `#regulation`, `#open-source`

---

<a id="item-9"></a>
## [Netherlands Seizes 800 Servers, Arrests 2 for Cyberattack Infrastructure](https://krebsonsecurity.com/2026/05/netherlands-seizes-800-servers-arrests-2-for-aiding-cyberattacks/) ⭐️ 6.0/10

Dutch authorities seized 800 servers and arrested 2 individuals for operating infrastructure that was used to support cyberattacks. The operation targeted what authorities identified as front companies providing hosting services specifically designed to facilitate cybercriminal activities. This operation demonstrates law enforcement's continued efforts to dismantle the infrastructure that enables large-scale cyberattacks and cybercriminal operations. Removing hosting infrastructure used by threat actors disrupts their ability to launch attacks and can help protect potential victims across the globe. The seized servers were operated by what community observers describe as front companies directly connected to Russian intelligence, rather than legitimate hosting providers offering services to regular customers. The Netherlands has become a notable jurisdiction for hosting malicious infrastructure, alongside Russia and China, making it a strategic location for law enforcement action.

hackernews · jruohonen · May 25, 13:56 · [Discussion](https://news.ycombinator.com/item?id=48266906)

**Background**: Cybercriminal hosting infrastructure refers to servers and data centers that are deliberately operated to support illegal online activities such as distributing malware, launching distributed denial-of-service (DDoS) attacks, or hosting command-and-control servers for botnets. Some jurisdictions, including the Netherlands, have historically been attractive to cybercriminals because of lax enforcement, permissive regulations, or connections to state-sponsored actors. Law enforcement agencies worldwide have increasingly prioritized disrupting this infrastructure as a way to prevent cyberattacks at their source.

**Discussion**: Community members expressed both technical interest and ethical puzzlement about the operation. Commenters noted that the seized infrastructure was operated by front companies with direct ties to Russian intelligence rather than legitimate hosting providers, and discussed why the Netherlands has become a hub for malicious hosting alongside Russia and China. Some observers with cybersecurity backgrounds expressed surprise at the level of engineering expertise devoted to supporting criminal infrastructure, questioning why skilled individuals would choose cybercrime over legitimate work.

**Tags**: `#cybersecurity`, `#law-enforcement`, `#infrastructure`, `#cybercrime`, `#threat-intelligence`

---

<a id="item-10"></a>
## [Datasette 1.0a30 adds customizable Jump menu with plugin extensibility](https://simonwillison.net/2026/May/24/datasette/#atom-everything) ⭐️ 6.0/10

Datasette 1.0a30 introduces a new customizable "Jump to..." menu accessible by pressing the forward slash (/) key, which filters databases, tables, and debug options as users type. The release also adds a new jump_items_sql() plugin hook that allows plugins to contribute their own items to the searchable menu, with datasette-agent 0.1a4 already leveraging this to add an AI chat interface. This feature improves user experience by providing quick navigation within Datasette instances and demonstrates the tool's commitment to extensibility through its plugin architecture. The ability for third-party plugins to integrate seamlessly into core UI elements like the Jump menu makes Datasette more flexible for different use cases and workflows. The Jump menu is triggered by pressing the forward slash key and dynamically filters results as users type, showing matching databases, tables, and other options. The new jump_items_sql() plugin hook enables developers to register custom items that appear in the menu, as demonstrated by datasette-agent which uses the makeJumpSections() JavaScript plugin hook to add a "Start a new agent chat" interface.

rss · Simon Willison · May 24, 23:52

**Background**: Datasette is an open-source multi-tool for exploring and publishing data, allowing users to import data from CSVs, JSON, database connections, and other sources. The tool features a plugin architecture that enables developers to extend functionality through hooks—a pattern where plugins can register callbacks that execute at specific points in the application lifecycle. Plugin hooks allow third-party extensions to integrate deeply with Datasette's core features without modifying the main codebase.

<details><summary>References</summary>
<ul>
<li><a href="https://datasette.io/">Datasette : An open source multi- tool for exploring and publishing data</a></li>
<li><a href="https://github.com/simonw/datasette">GitHub - simonw/ datasette : An open source multi- tool for exploring...</a></li>

</ul>
</details>

**Tags**: `#datasette`, `#database-tools`, `#plugin-architecture`, `#ui-features`, `#python`

---

<a id="item-11"></a>
## [Developer Recreates 1980s Usborne 'Mad House' Game Using Claude AI](https://simonwillison.net/2026/May/24/usborne-mad-house/#atom-everything) ⭐️ 6.0/10

Simon Willison has recreated the classic 1983 Usborne computer game 'Mad House' from the book 'Creepy Computer Games' as an interactive JavaScript/HTML web version. He used Claude AI to convert the original BASIC code from the freely available Usborne PDF into a modern, mobile-friendly web game with a retro green-on-black terminal aesthetic. This project demonstrates a practical workflow for using modern AI assistants to rapidly recreate and modernize legacy software, making nostalgic computing experiences accessible to new audiences through web browsers. It also highlights how the recent release of free Usborne programming book PDFs enables developers to engage with computer history and educational computing traditions from the 1980s. The recreation maintains the original game mechanics where players navigate ASCII-based corridors and manage doors to avoid footsteps, using keyboard controls (X/C for near doors, N/M for far doors). The implementation is built entirely in vanilla JavaScript with no external frameworks, ensuring lightweight performance and easy deployment as a standalone web tool.

rss · Simon Willison · May 24, 17:14

**Background**: Usborne was a UK publisher famous for its 1980s computer books that taught programming through illustrated, hands-on projects—many readers learned to code by typing in BASIC programs from these books on home computers like the Commodore 64. The original 'Mad House' game was a text-based adventure where players had to manage doors in a haunted house to avoid an unseen threat, a common game type in early home computing. Claude is an AI assistant created by Anthropic that can understand code, generate new code, and help developers build applications through natural language prompts.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/platform/api">Claude Platform | Claude</a></li>
<li><a href="https://www.anthropic.com/learn/build-with-claude">Anthropic Academy: Claude API Development Guide \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#retro-computing`, `#game-development`, `#AI-assisted-coding`, `#web-development`, `#nostalgia`

---