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
title: References
---

<div class="border-b border-neutral-800 pb-6 text-4xl mb-6"><twemoji:books />&nbsp; References </div>

<div class="grid grid-cols-2 gap-10 text-xs leading-none">
  <div>SC World. (2025, July 11). Fake Visual Studio Code extension for Cursor led to $500k theft. https://www.scworld.com/news/fake-visual-studio-code-extension-for-cursor-led-to-500k-theft
  </div>
  <div>Col 2
  </div>
</div>
<div class="text-sm mt-8 border-t pt-4 italic">Reflections, structure, and design are by Josh Miller. Collaborated with ChatGPT to create visuals.</div>
