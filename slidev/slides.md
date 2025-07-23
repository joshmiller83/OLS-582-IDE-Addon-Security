---
theme: default
layout: image
image: assets/ChatGPT-slide1.png
title: Josh Miller’s IDE Add-On Security Proposal (OLS-582)
info: |
  ## Summer 2025
  This proposal explores the hidden security risks of IDE add-ons and offers a vision for how the Urban Institute can lead by example during Cybersecurity Awareness Month. Our goal: help researchers, developers, and leaders understand the stakes—and take smarter, scalable action.
drawings:
  persist: false
transition: fade
mdc: true
fonts:
  sans: IBM Plex Sans
  weights: '100,200,300,400,500,600,700'
  italic: true

favicon: 'assets/ide-addon-favicon.ico'
---

<div class="text-center mt-12 text-5xl font-thin mb-5 text-left"><span class="font-black">What’s Hiding in Your Code Editor?</span></div>
<h2 class="text-red-400">OLS-582</h2>

<p class="pt-12 pb-12 pr-96 text-red-200">
This proposal explores the hidden security risks of <br>IDE add-ons and offers a vision for how the Research Tech Office at Urban Institute can lead by example during Cybersecurity Awareness Month. <br><br>Our goal: help researchers, developers, and leaders understand the stakes—and take smarter, scalable action.
</p>

<div class="absolute bottom-10">
  <span class="font-700">
    <logos:linkedin-icon /> &nbsp; <a href="https://www.linkedin.com/in/josh3/" target="_blank">Josh Miller</a> &nbsp; &nbsp; &nbsp; <twemoji-spiral-calendar /> &nbsp;<span class="text-red-300">Last updated:</span>&nbsp; July 20, 2025
  </span>
</div>

<div class="abs-br mr-12 mb-8 text-xl">
  <a href="https://github.com/joshmiller83/OLS-582-IDE-Addon-Security" target="_blank" class="slidev-icon-btn">
    <logos:git-icon />
  </a>
</div>


---
title: Setting it up, Part 1
layout: image
image: assets/ChatGPT-slide1.png
---


# Before we get into it

<div class="text-white text-2xl mt-10 italic">Context: This presentation is designed to be given to Urban Institute Stakeholders. However, this slide (and a few others that follow) are not part of the final presentation. These slides give context to my plans for this change vision.</div>

---
title: Setting it up, Part 2
layout: image
image: assets/ChatGPT-slide1.png
---

# Before we get into it

<v-clicks depth="2" class="mt-10 text-xl">

- Organizational Context: Urban Institute is a Non-Profit Research Organization (some call it a think-tank). _**Our reputation is our hedgehog.**_
  - Hedgehog: Drive impact by Decision Makers at local, state, and national levels by providing evidence-based research.
  - Distributed research divisions that write Python and R.
- Change Vision: IDE Add-ons are an important, invisible, unregulated attack vector.
  - Feasible, focused, communicable.
  - Address using awareness efforts led by a coalition of the willing.
- Kotter's (1996) "Step 1" sense of urgency is going to come from headlines.

</v-clicks>

<!-- 
Urban Institute is a Non-Profit Research Organization (some call it a think-tank). Our reputation is _everything_.

While our IT is centralized, our programmers are distributed through-out dozens of different Research Divisions.

Our Hedgehog is simple, we want to impact the world for the better through evidence based research. This security vector directly threatens our ability to do that.

The problem is simple, Urban Institute has reputational, operational, and legal risks surrounding the security of our coding environments. I have identified an important attack vector that we have been
ignoring: The IDE Addon or Extension. If you are unaware, programmers use software to write code. This 
software is usually a general or unique use platform for additional third party plugins that support 
your unique environment. Do you want an AI to help you write tests? How about syntax highlighting? How about connecting to a database or terminal? Many of these features require third party software to be installed on our systems. Most importantly, the average programmer knows to only install legitimate looking extensions (ones that have hundreds of thousands of installs, high ratings, etc), but the platform's marketplaces are not always as secure as we think. 

I will tie this into a headline for a sense of urgency. Show people what's at stake.
-->

---
title: Setting it up, Part 3
layout: image
image: assets/ChatGPT-slide1.png
---

<div class="grid grid-cols-2 gap-10">
<div class="text-2xl">

# Burke-Litwin Model

<div class="mt-10">

- Links leadership, culture, and external drivers
- Our culture and mission (transformational elements) fit this change.
- Leadership / stakeholders have recommended us to proceed

</div>
</div>
<div>

```mermaid
graph TD
    A[External<br>Environment] <--> C[Mission &<br>Strategy]
    A <--> D[Organisation<br>Culture]
    D <--> J

    C <--> F[Work Unit<br>Climate]
    F <--> G[Employee<br>Motivation]
    D <--> H[Tasks &<br>Skills]
    H <--> I[Needs &<br>Values]

    C <--> J[Leadership]
    J <--> K[Structure]

    G <--> L[Organizational<br>Performance]
    I <--> L
```

</div>
</div>

---
title: Setting it up, Part 4
layout: image
image: assets/ChatGPT-slide1.png
---

# Let's dive in!

<div class="text-white text-2xl mt-10 italic">The following slides are the presentation I plan to record and send out to all programmers, calling for a coalition of the willing.</div>

---
title: Start Coalition Building Presentation
layout: image
image: assets/ChatGPT-slide1.png
---

<div class="text-center mt-12 text-5xl font-thin mb-5 text-left"><span class="font-black">What’s Hiding in Your Code Editor?</span></div>

<p class="pt-12 pb-12 pr-96 text-red-200 text-2xl">
This proposal explores the hidden security risks of IDE add-ons and offers a vision for how we can raise some awarness and support our mission of impact. <br><br>The goal: help researchers, developers, and leaders understand the stakes—and take smarter, scalable action.
</p>

---
title: The Risk
layout: image
image: assets/ChatGPT-slide2-v2.png
---

<div class="pb-6 text-thin text-4xl">One unvetted add-on quietly exfiltrated everything.</div>
<div class="grid grid-cols-2 gap-10">
<div class="pr-20">
  <div v-click class="mb-4"><span class="inline-block -ml-8 mr-3"><twemoji-money-with-wings /></span>
  <span class="font-medium">Just a few days ago</span>
  <span class="text-purple-200">, a developer lost $500,000 after installing a fake VSCode extension.</span></div>
  
  <div v-click class="mb-4"><span class="inline-block -ml-8 mr-3"><twemoji-magic-wand /></span>
  <span class="font-medium">The attacker manipulated the VS Code Marketplace </span>
  <span class="text-purple-200">to make the malicious plugin appear trustworthy.</span></div>

  <div v-click class="mb-4"><span class="inline-block -ml-8 mr-3"><twemoji-bug /></span>
  <span class="font-medium">Once installed, the add-on deployed malware </span></div>

  <div v-click class="mb-4"><span class="inline-block -ml-8 mr-3"><twemoji-boomerang /></span>
  <span class="font-medium">Even after removal, the attacker returned </span>
  <span class="text-purple-200">with slight name changes and similar download manipulation.</span></div>
</div>
<div class="pl-32 -mr-1">
  <div v-click class="mb-18"><span class="inline-block -ml-8 mr-3"><twemoji-warning /></span>
  <span class="font-medium">This was a systemic blind spot. </span>
  <span class="text-purple-200">Organizations need their own controls, awareness, and policy frameworks.</span></div>

  <div v-after class="text-right italic text-purple-300">Source: <a href="https://www.scworld.com/news/fake-visual-studio-code-extension-for-cursor-led-to-500k-theft" target="_blank">SCWorld (July 2025)</a></div>
</div>
</div>

---
title: What Are IDE Add-Ons
layout: image
image: assets/ChatGPT-slide3.png
---

<div class="grid grid-cols-2 gap-10">
  <div class="pt-32 pr-6">
    <div v-click class="pb-6 text-thin text-3xl text-purple-200">What Are IDE Add-Ons?<br><span class="text-white italic">Why Should We Care?</span></div>
    <div v-click class="mt-24 text-red-200 text-2xl text-thin pr-14">These are extensions we use in VS Code, RStudio, PHPStorm, Cursor, etc. to improve productivity.</div>
  </div>
  <div class="pt-14 pl-30 text-red-200 text-2xl text-thin">
    <div v-click class="pt-32">IDE Addons often run with full access to your terminal, files, repositories, possibly environment secrets.</div>
  </div>
</div>


---
title: Urban Institute is Vulnerable Today
layout: image
image: assets/ChatGPT-slide4.png
---

<div class="grid grid-cols-2 gap-10">
  <div class="pt-32 pr-6">
    <div v-click class="font-thin text-5xl text-purple-200">Urban Institute Development Environments Are Vulnerable Today</div>
    <div v-click class="mt-8 text-purple-200 text-2xl font-medium pr-14 italic">We have no formal plugin review process.</div>
  </div>
  <div class="pt-14 pl-16 -mr-6 text-purple-200 text-2xl font-medium pr-14 italic">
    <div v-click class="pt-20 mb-32">Add-ons can access: Private repos, Internal data, Shared Network Drives</div>
    <div v-click class="pt-5">Developers install them with good intent—but there’s no shared guardrails.</div>
  </div>
</div>


---
title: Why Now?
layout: image
image: assets/ChatGPT-slide5.jpg
---

<div class="grid grid-cols-2 gap-10">
  <div>
    <div v-click class="text-4xl text-red-200 mb-2 mt-16">Why Now?</div>
  </div>
  <div class="text-2xl">
    <div v-click class="mb-2"><twemoji-check-mark-button class="-ml-12" /> &nbsp; External threats are more sophisticated.</div>
    <div v-click class="mb-2"><twemoji-check-mark-button class="-ml-12" /> &nbsp; Internal practices are uneven.</div>
    <div v-click><twemoji-check-mark-button class="-ml-12" /> &nbsp; October gives us a natural moment to educate and align.</div>
  </div>
</div>

---
title: Proposal
layout: image
image: assets/ChatGPT-slide6.png
---

<div class="text-white text-md grid grid-cols-2 gap-20 mt-40">

  <div class="text-2xl ml-12">

   <div class="text-4xl font-black mb-8 text-cyan-200">The Proposal</div>

  <div v-click class="mb-6"><twemoji-eye class="-ml-12" /> &nbsp; <strong class="text-purple-200">Awareness</strong>: Lunch talk, Slack tip, and simple visuals about plugin risk.</div>
  <div v-click class="mb-2"><twemoji-shield class="-ml-12" /> &nbsp; <strong>Guidance</strong>: Lightweight, co-authored “Plugin Vetting” best practices.</div>
  </div>
  <div class="text-2xl ml-12 mt-18">
  <div v-click class="mb-6"><twemoji-family-woman-girl-boy class="-ml-12" /> &nbsp; <strong>Pilot</strong>: A volunteer group to review current plugin usage<br>and create guidance.</div>
  <div v-click><twemoji-spiral-calendar class="-ml-12" /> &nbsp; <strong>Timeline</strong>: Plan to launch guardrails by October.</div>
  </div>
</div>

---
title: What Success Looks Like
layout: image
image: assets/ChatGPT-slide7.png
---

# What Success Looks Like
<div class="text-white text-2xl mt-10 ml-96 pl-24">

* Developers understand the risk.
* Teams have a clear, practical way to assess plugins.
* We’ve piloted guidance in one or two dev-heavy teams.

</div>
---
title: Built to Fit Our Culture
layout: image
image: assets/ChatGPT-slide8.png
---

# Built to Fit Our Culture

<div class="text-white text-xl mt-30 pr-56 mr-56">

* Not a mandate. No one’s blocking extensions.
* Built by devs, for devs—fast feedback loops.
* Respects Urban’s Divisions' independence while nudging us toward security.

</div>
---
title: Low Lift, High Value
layout: image
image: assets/ChatGPT-slide9.png
---

<div class="grid grid-cols-2 gap-10">
  <div></div>
  <div class="mt-42 text-2xl">

# Low Lift, High Value
* No new tools needed.
* No new software to deploy.
* Just clarity, visibility, and smarter habits.

</div></div>

---
title: Want to Help?
layout: image
image: assets/ChatGPT-slide10.png
---

<div class="grid grid-cols-2 gap-10">
  <div></div>
  <div class="mt-12 -mr-12 pl-24 text-2xl text-white">

# Want to Help?

<div class="text-2xl text-white mt-10 mb-4">I’m asking for volunteers to</div>

* Draft best practices
* Share what's working
* Pilot ideas in October

<div class="text-2xl text-white mt-4 mb-4 italic">No long meetings. Just honest feedback and a little collaboration.</div>

</div></div>

---
title: Q&A
layout: image
image: assets/ChatGPT-slide11.png
---

<div class="text-5xl text-purple-200 text-center font-thick italic mt-36">I want your feedback and<br>I'm open to questions</div>
<div class="grid grid-cols-2">
<div class="text-white text-2xl italic mt-10 leading-tight pr-24">“What would make this effort useful to your team?”</div>
<div class="text-white text-2xl italic mt-10 leading-tight pl-24 -mr-12">“What concerns do you<br>have about vetting<br>plugins?”<br><br>“Who else should I talk to?”
</div>
</div>

---
title: Future is bright
layout: image
image: assets/ChatGPT-slide12.png
---

<div class="ml-36 text-5xl text-purple-200 text-center font-thick italic mt-10">Thank you for your time!</div>

<div class="ml-36 text-white text-2xl mt-10 text-center">Securing our development<br>environments is critical to our<br>ability to make impact.</div>

<div class="ml-36 text-white text-2xl mt-10 text-center">Contact <strong>Josh Miller</strong> if interested<br>in joining the coalition.</div>

---
title: References
---

<div class="border-b border-neutral-800 pb-6 text-4xl mb-6"><twemoji:books />&nbsp; References </div>

<div class="text-2xl">
  <div>Burke, W. W. (2011). Organization change: Theory and practice (3rd ed.). Sage Publications.<br><br> Kotter, J. P. (1996). Leading change. Harvard Business School Press.<br><br>SC World. (2025, July 11). Fake Visual Studio Code extension for Cursor led to $500k theft. https://www.scworld.com/news/fake-visual-studio-code-extension-for-cursor-led-to-500k-theft</div>
</div>
<div class="text-2xl mt-12 border-t pt-8 italic">Reflections, structure, and design are by Josh Miller. Collaborated with ChatGPT to create visuals.</div>
