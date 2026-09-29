<div align="center">

# 🛡️📱 Android Security Roadmap

**A practical, resource-linked path from zero to Android Application Pentester — built around real courses and hands-on labs, with a clear checkpoint for the [eMAPT](https://security.ine.com/certifications/emapt-certification/) certification.**

*Track your progress with the checkboxes. Open it, see the last thing you ticked, continue from there.*

</div>

---

## 🎯 Who this is for & the goal

This roadmap is for anyone who wants to learn **Android application penetration testing / mobile bug bounty** in a structured way instead of jumping randomly between tutorials.

- **Primary milestone:** reach **eMAPT exam readiness** (see the 🏁 checkpoint below), sit the exam, then continue to advanced mastery.
- **End state:** you can take any APK, reverse it, analyze it statically and dynamically, exploit its components, bypass root/SSL-pinning, hook it with Frida, and write it up.

> **Assumed study pace:** ~**20 hours/week** (≈ 4 h/day × 5 days). All time estimates below assume this pace. If you already program or already do web bug bounty, you'll move faster through the language and network phases.

---

## 🧭 How to use this roadmap

1. Go top to bottom. Each phase lists **what to learn**, the **exact resources**, **hands-on practice**, and a **"Done when…"** line.
2. **Tick the checkboxes** as you finish. Your last tick = where you resume.
3. Don't aim for perfection on developer-only material — for security you need to **read** code fluently, not ship production apps (see Phase 0).
4. At the 🏁 checkpoint, decide whether to sit **eMAPT**; you can take it before doing the advanced phases.

**Legend:** 🎥 video · 📖 read · 🧪 lab/practice · ⭐ high priority · ⏭️ skim or skip · 🏁 milestone

---

## 📚 Core resources used in this roadmap

| Resource | Use | Link |
|----------|-----|------|
| 🎥 Mohamed El Desouky — Java for Beginners **(🇪🇬 Arabic)** | Java language core | [Playlist](https://www.youtube.com/playlist?list=PL1DUmTEdeA6K7rdxKiWJq6JIxTvHalY8f) |
| 🎥 Mohamed El Desouky — OOP with Java **(🇪🇬 Arabic)** | Object-oriented Java | [Playlist](https://www.youtube.com/playlist?list=PL1DUmTEdeA6Icttz-O9C3RPRF8R8Px5vk) |
| 🎥 Java Full Course **(🌐 English)** | Java language core — English alternative | [Video](https://www.youtube.com/watch?v=A74TOX803D0) |
| 🎥 freeCodeCamp — Android Development for Beginners **(🌐 English)** | Android app-dev concepts | [Video](https://www.youtube.com/watch?v=fis26HvvDII) |
| 🎓 INE — Mobile App Security & Pentesting (MASPT) | **eMAPT prep** — use *if available*; if not, the other resources are enough | [INE](https://security.ine.com/) |
| 🎥 Udemy — Android App Hacking: Black Belt Edition | Deep hands-on hacking | [Course](https://www.udemy.com/course/android-app-hacking-black-belt-edition/) |
| 🧩 Hextree.io — Android Security Map | Modern, structured labs | [Hextree](https://app.hextree.io/map/android) |
| 📖 OWASP MASTG / MASVS | The reference standard | [MASTG](https://mas.owasp.org/MASTG/) |
| 📖 Oversecured blog checklists | Deep-dive checklists | [Blog](https://blog.oversecured.com/) |

---

## Phase 0 — Programming Foundation (Java → reading level, + a taste of Kotlin)

> **Why:** as a pentester you mostly **read** decompiled code. When you decompile an APK with `jadx`, even Kotlin apps show up as **Java**. So Java literacy is your core tool. Goal = read code fluently, **not** become a production app developer.

**How to study this phase:** *code along* actively for the fundamentals & OOP (don't just watch). For pure UI/design parts of the freeCodeCamp course, watch at 1.5–2× just for familiarity.

### 0.1 — Java language core ⭐ (study all)

> 🌐 **Choose your language and finish one:**
> - **🇪🇬 Arabic:** El Desouky *Java for Beginners* (episode checklist below).
> - **🌐 English:** [Java Full Course](https://www.youtube.com/watch?v=A74TOX803D0) — same fundamentals.

<details><summary>El Desouky (Arabic) episode checklist (click to expand)</summary>

- [ ] 00 Introduction
- [ ] 01 What is programming?
- [ ] 02 How to Install Java
- [ ] 03 Your First Program
- [ ] 04 Displaying Program Output
- [ ] 05–06 Input and Variables (Part 1–2)
- [ ] 07–08 Arithmetic Operators (Part 1–2)
- [ ] 09–10 IF statement (Part 1–2)
- [ ] 11–12 Switch statement (Part 1–2)
- [ ] 13 While Loop (+ 13.1, 13.2 Flag-Controlled While)
- [ ] 14 Do-While Loop
- [ ] 15 For Loop
- [ ] 16 Break & Continue
- [ ] 17 Revision on Loops & Conditionals
- [ ] 18 Introduction to Methods
- [ ] 19 Methods With Parameters
- [ ] 20 Methods & Variable Scope
- [ ] 21 Methods Overloading
- [ ] 22 Arrays
- [ ] 23 Arrays and Methods
- [ ] 24 Two-Dimensional Arrays
</details>

### 0.2 — Object-Oriented Java — 🎥 El Desouky *OOP with Java* ⭐ (study all — this is the most important part)
<details><summary>Episode checklist (click to expand)</summary>

- [ ] 00 Get Started
- [ ] 01–03 What is OOP? (Part 1–3)
- [ ] 04–07 Create Your First Class (Part 1–4)
- [ ] 08–09 Constructors & Constructor Overloading (Part 1–2)
- [ ] 10 Static Methods and Fields
- [ ] 11 Passing an Object to a Method
- [ ] 12 Comparing and Copying Objects
- [ ] 13–14 Inheritance and Polymorphism (Part 1–2)
- [ ] 15 Inheritance and Method Overriding
- [ ] 16 Final Methods and Protected Members
- [ ] 17 Abstract Class and Abstract Method
- [ ] 18 Interfaces
- [ ] 19 Enum
- [ ] 20 Exception Handling
- [ ] 21 ArrayList Class
- [ ] Revision on OOP (Parts 1–4) — optional
</details>

### 0.3 — Android concepts (from freeCodeCamp) — study the security-relevant parts only
- [ ] ⭐ Java refresher + OOP sections (if you skipped El Desouky) 
- [ ] ⭐ **Intents** (Create App's First Page - Intents)
- [ ] ⭐ **SharedPreferences + Gson** (data persistence — future *insecure storage* target)
- [ ] ⭐ **WebView** (Show Your Website in a WebView — future *WebView* attack surface)
- [ ] ⏭️ Skim: Layouts, ListView/Spinner, Material Design, RecyclerView, Fonts, Animations, CardView *(developer polish — low priority for security)*

### 0.4 — Kotlin (reading level, after Java) 📖
> ℹ️ **Optional at this foundation stage** — Java alone is enough to get started. But it's **strongly recommended later as you advance**, since most modern Android apps are written in Kotlin.
- [ ] Null-safety (`?`, `!!`), `data class`, `when`/`sealed`, lambdas & higher-order functions, extension functions, basic coroutines — enough to *read* modern apps. [Kotlin Koans](https://play.kotlinlang.org/koans)

**Done when:** you can read an unfamiliar Java class (and a Kotlin one) and explain what it does — classes, inheritance, interfaces, collections, exceptions.
**⏱️ Estimate:** ~2–3 weeks.

---

## Phase 1 — Android Fundamentals & Security Model

> **Why:** you can't attack what you don't understand. Learn how Android apps are built, isolated, and permitted.

**Learn:**
- [ ] Android OS architecture (basics) & the **app sandbox** (UID separation)
- [ ] **Permission model** (install-time vs runtime, dangerous permissions)
- [ ] **APK structure** (`AndroidManifest.xml`, `classes.dex`, resources, `lib/`)
- [ ] The **app components** and how each is attacked: **Activity, Fragment, Service, BroadcastReceiver, ContentProvider, Intents**

**Resources:**
- 🎥 Udemy *Black Belt* → **App structure** section: *Filestructure of an APK, Dalvik/Dex, AndroidManifest.xml, App-Permissions, Activities, Intents, BroadcastReceiver, Services, ContentProvider* (theory parts)
- 🧩 Hextree → Android map: components / Intent attack surface
- 📖 OWASP MASTG "Android Platform Overview" + 📖 Oversecured component checklists

**Done when:** you can list an app's components from its Manifest and say how each *could* be exposed.
**⏱️ Estimate:** ~1 week (faster if you already know Linux permissions).

---

## Phase 2 — Static Analysis & Reverse Engineering

> **Why:** read an app's code without running it — find secrets, logic, and bugs.

**Learn:**
- [ ] Decompiling: **jadx / jadx-gui**, **dex2jar**, **apktool**
- [ ] Reading recovered **Java** and an intro to **smali**
- [ ] **Static findings:** insecure logging, hardcoded secrets/keys, insecure data storage, weak crypto usage
- [ ] Automated static analysis with **MobSF**
- [ ] Intro to **call graphs / flow graphs** (androguard) for obfuscated apps

**Resources:**
- 🎥 Udemy *Black Belt* → **Reverse Engineering** section: *Dex2Jar, Jadx-Gui (+HandsOn), Reversing Apps, Creating a CallGraph/FlowGraph*
- 🎥 Udemy *Black Belt* → **Decompiling – Preparation/HandsOn**
- 🧪 Practice: **DIVA**, **InsecureShop** (static parts), **DroidSiege**

**Done when:** you can decompile any APK, find hardcoded secrets/insecure storage, and read the relevant smali.
**⏱️ Estimate:** ~1.5 weeks.

---

## Phase 3 — Dynamic Analysis, Network & Component Exploitation

> **Why:** attack the app while it runs — its components and its traffic. *(Your web-bug-bounty background makes the network part fast.)*

**Learn:**
- [ ] **adb** deep usage (shell, `am`, `pm`, port-forwarding)
- [ ] **Drozer** (component enumeration & exploitation — very relevant for eMAPT)
- [ ] Exploiting **exported Activities / Services / BroadcastReceivers**
- [ ] **ContentProvider** attacks: **SQL injection** & **path traversal**
- [ ] **Deep links / App links** testing
- [ ] **WebView** security & `JavaScriptInterface` abuse, XSS/SQLi in WebViews
- [ ] **Traffic interception** with **Burp** (HTTP + HTTPS), installing a CA

**Resources:**
- 🎥 Udemy *Black Belt* → **Activities/Intents Hacking, DeepLinks (2024), BroadcastReceiver Hacking, ContentProvider – SQL Injection / Path Traversal**
- 🎥 Udemy *Black Belt* → **Man-in-the-Middle** section: *Burp Setup, HTTPS technical view, Installing a Certificate*
- 🧩 Hextree → WebView & Intent attack-surface labs · 📖 [Oversecured WebView checklist](https://blog.oversecured.com/Android-security-checklist-webview/)
- 🧪 Practice: **InjuredAndroid**, **AndroGoat**, **DroidSiege**, **InsecureShop**

**Done when:** you can enumerate & exploit exported components, dump a vulnerable ContentProvider, and intercept an app's HTTPS traffic.
**⏱️ Estimate:** ~1.5–2 weeks.

---

## Phase 4 — Runtime Manipulation (Frida / objection / bypasses)

> **Why:** hook a running app, change its behavior, and defeat client-side protections.

**Learn:**
- [ ] **Frida** basics: `Java.use`, `Java.choose`, hooking methods, overloads, timing
- [ ] **objection** (Frida-powered) for quick wins
- [ ] **Root detection** — how it works & how to bypass (Frida + smali)
- [ ] **SSL/Certificate pinning** — detect & bypass (Frida/objection + smali patch)
- [ ] Tooling: **Magisk**, **MobSF** (dynamic), **Medusa** framework

**Resources:**
- 🎥 Udemy *Black Belt* → **FRIDA** section: *Install, Hooking Theory, Observing/Modifying Parameters, Function Overloading, Rooting Detection bypass, Actively calling a method, Working with Instances*
- 🎥 Udemy *Black Belt* → **Certificate Pinning**: *Patching Fingerprint/Certificate, Objection Bypass*
- 🧩 Hextree → dynamic instrumentation & bypass labs
- 🧪 Practice: **Damn Vulnerable Bank** (root/Frida/SSL bypass), **DroidSiege** advanced tiers

**Done when:** you can bypass a root check and SSL pinning on a real app and hook a method to change its result.
**⏱️ Estimate:** ~1.5–2 weeks.

---

## 🏁 eMAPT Exam Readiness Checkpoint

After Phases 1–4 and the practice labs, you are ready to sit **[eMAPT](https://security.ine.com/certifications/emapt-certification/)**. If you have access to the **INE MASPT** course, use it as the official prep spine; **if not, the rest of the resources here are enough** to prepare.

**About the exam (verify current details on INE):** eMAPT is a **practical** certification — you're given a vulnerable mobile app and must **develop a working exploit** and document it, on your own time (multi-day). It is entry-to-intermediate and focuses on Android app pentesting methodology, not niche SMALI/game-hacking.

**Readiness checklist — you should be able to:**
- [ ] Reverse an APK and read its Java/smali
- [ ] Enumerate & exploit exported components (Activities, Receivers, Services)
- [ ] Exploit an insecure ContentProvider (SQLi / path traversal)
- [ ] Find insecure storage / hardcoded secrets / weak crypto
- [ ] Intercept & manipulate HTTPS traffic (Burp + CA)
- [ ] Bypass root detection & SSL pinning (Frida/objection or smali)
- [ ] Use Drozer & Frida comfortably
- [ ] Write a clear vulnerability report / PoC

**➡️ Plan:** finish INE MASPT → tick the list above → **sit eMAPT** → then continue Phase 5+. You do **not** need the entire Black Belt course (esp. the heavy SMALI/game-hacking) before the exam.

**⏱️ Estimate to this checkpoint from zero:** ~**8–12 weeks** at 20 h/week (toward the lower end given a web-security background).

---

## Phase 5 — Advanced Topics (recommended after the exam)

**Learn:**
- [ ] **SMALI patching** deep-dive (registers, opcodes, control-flow, code injection) — 🎥 Udemy *Black Belt* **SMALI** chapter
- [ ] **Native / NDK** reversing & hooking — Frida on C/C++, **Ghidra** — 🎥 Udemy *Black Belt* NDK + Ghidra videos
- [ ] **Intent redirection**, **dirty stream**, **dynamic code loading** vulns, **biometric auth** bypass
- [ ] **Cross-platform apps** (how reversing/hooking differs): **Flutter, React Native, Xamarin, Cordova, Capacitor**
- [ ] **Advanced Frida**: gadgets, RPC exports, `Interceptor.attach/replace`, inline hooking, basic **RASP** handling
- [ ] 🎥 Udemy *Black Belt* → **CTF series** (LicenseValidator/Ghidra, AndroGoat) for consolidation

**⏱️ Estimate:** ongoing, ~3–5 weeks of focused work.

---

## Phase 6 — Practice Labs (use throughout, not just at the end)

| Lab | Focus | Link |
|-----|-------|------|
| 🧪 **DroidSiege** | Intentionally vulnerable app with graded difficulty levels across the OWASP MASVS classes | [repo](https://github.com/0xsl4m/DroidSiege) |
| 🧪 InjuredAndroid | CTF-style beginner | [repo](https://github.com/B3nac/InjuredAndroid) |
| 🧪 DIVA | Classic fundamentals | [repo](https://github.com/payatu/diva-android) |
| 🧪 AndroGoat | Kotlin, broad coverage | [repo](https://github.com/satishpatnayak/AndroGoat) |
| 🧪 InsecureShop | Realistic, unrooted-friendly | [repo](https://github.com/hax0rgb/InsecureShop) |
| 🧪 Allsafe | Progressive difficulty | [repo](https://github.com/t0thkr1s/allsafe-android) |
| 🧪 Mobile Hacking Lab | Free guided labs | [site](https://www.mobilehackinglab.com/free-mobile-hacking-labs) |
| 🧪 8kSec | Exploitation challenges | [academy](https://academy.8ksec.io/course/android-application-exploitation-challenges) |
| 🧪 Hextree Android Map | Modern, structured | [Hextree](https://app.hextree.io/map/android) |

---

## 🧰 Tools checklist

- [ ] `adb`, `scrcpy`  · [ ] **jadx / jadx-gui** · [ ] **apktool** · [ ] **dex2jar** · [ ] **androguard**
- [ ] **Frida** · [ ] **objection** · [ ] **Drozer** · [ ] **MobSF** · [ ] **Burp Suite** · [ ] **Magisk** · [ ] **Medusa** · [ ] **Ghidra**

---

## 🗺️ At-a-glance plan

| Phase | Focus | Main resource | Est. time | Status |
|-------|-------|---------------|-----------|--------|
| 0 | Java + OOP (reading level) | El Desouky (AR) + freeCodeCamp | 2–3 wk | ⬜ |
| 1 | Android fundamentals & security model | Black Belt / Hextree / MASTG | ~1 wk | ⬜ |
| 2 | Static analysis & RE | Black Belt / MobSF | ~1.5 wk | ⬜ |
| 3 | Dynamic, network & components | Black Belt / Drozer / Burp | 1.5–2 wk | ⬜ |
| 4 | Runtime manipulation (Frida) | Black Belt / Hextree | 1.5–2 wk | ⬜ |
| 🏁 | **eMAPT readiness** (INE MASPT if available, else the rest is enough) | INE MASPT / this roadmap | **~8–12 wk total** | ⬜ |
| 5 | Advanced (SMALI, native, cross-platform) | Black Belt / Ghidra | 3–5 wk | ⬜ |
| 6 | Practice labs | *(throughout)* | ongoing | ⬜ |

---

## 📖 Reference & standards

- [OWASP MASTG](https://mas.owasp.org/MASTG/) · [OWASP MASVS](https://mas.owasp.org/MASVS/) · [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/)
- [Oversecured blog](https://blog.oversecured.com/) · [HackTricks — Mobile](https://book.hacktricks.xyz/mobile-pentesting/android-app-pentesting)

---

<div align="center">

*Made for learners. Contributions & suggestions welcome — open an issue or PR.*

</div>
