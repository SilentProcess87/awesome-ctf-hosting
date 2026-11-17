# Awesome CTF Hosting [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of platforms for **running** a Capture The Flag event, with a side-by-side comparison, a plain recommendation for each kind of organiser, and the places to play and practise.

> **Who maintains this:** [CTF-Hub](https://ctf-hub.io), which is one of the platforms listed. Entries about other products come from each project's own pages, docs or repository, checked in November 2026. Where something could not be confirmed there, the list says "not documented" instead of guessing. Corrections are welcome: see [Contributing](#contributing).

## Contents

- [Host your own CTF](#host-your-own-ctf)
  - [Open source, self-hosted](#open-source-self-hosted)
  - [Managed and vendor-hosted](#managed-and-vendor-hosted)
  - [Built for classrooms](#built-for-classrooms)
  - [Archived or dormant](#archived-or-dormant)
- [Comparison](#comparison)
- [Which one should you pick?](#which-one-should-you-pick)
- [Tools for organisers](#tools-for-organisers)
- [Play and practise](#play-and-practise)
- [Competitions worth knowing](#competitions-worth-knowing)
- [Other lists](#other-lists)
- [The egg](#the-egg)
- [Contributing](#contributing)

## Host your own CTF

### Open source, self-hosted

You run the servers; the software is free.

- [CTFd](https://github.com/CTFd/CTFd) - The most widely used jeopardy-style framework. Themes, plugins and a REST API. Apache-2.0. Per-player challenge instances need a third-party plugin on the open-source edition.
- [rCTF](https://github.com/otter-sec/rctf) - Scoreboard built for large public competitions, now maintained by OtterSec. CTFtime login, documented API, optional per-team instancer on Docker or Kubernetes. Apache-2.0.
- [GZCTF](https://github.com/GZTimeWalker/GZCTF) - ASP.NET Core platform with dynamic containers on Docker or Kubernetes and per-team dynamic flags built in. AGPL-3.0 core with additional restricted components.
- [RootTheBox](https://github.com/moloch--/RootTheBox) - "A Game of Hackers": a real-time scoring engine with game mechanics such as in-game money and an optional story mode. Apache-2.0.
- [kCTF](https://github.com/google/kctf) - Google's Kubernetes infrastructure for deploying and sandboxing challenges. It is **not** a scoreboard: pair it with CTFd or rCTF. Apache-2.0.
- [pwn.college DOJO](https://github.com/pwncollege/dojo) - The infrastructure behind pwn.college. An education platform more than a general event scoreboard. BSD-2-Clause.

### Managed and vendor-hosted

Someone else runs the platform; you bring the event.

- [CTF-Hub](https://ctf-hub.io) - Managed, multi-tenant platform for private, branded competitions and hands-on training with your own challenges. Container challenge instances from the Team plan; SAML SSO and LMS integration (LTI 1.3, SCORM, xAPI) on the higher plans. Free tier and published plans. No self-hosted edition; not open source.
- [CTFd hosted and Enterprise](https://ctfd.io/pricing/) - CTFd run for you, in published tiers, with your own domain. Enterprise can be self-hosted or on CTFd Cloud and adds isolated per-participant infrastructure.
- [Hack The Box CTF Marketplace](https://www.hackthebox.com/capture-the-flag) - Self-serve events assembled from Hack The Box's content library. Custom content is by request.
- [TryHackMe CTF Builder](https://tryhackme.com/resources/blog/new-ctf-builder) - Events assembled from TryHackMe's challenge pool, for Business and Education customers. Bespoke challenges are a separate service.
- [SkillBit](https://skillbit.com/) - Formerly MetaCTF. Competition-based training and events run as a service, plus a monthly public Flash CTF.
- [CyberTalents](https://cybertalents.com/competitions/host) - Hosted competitions on a ready challenge library, aimed at recruiting and talent assessment.
- [Root-Me PRO](https://root-me.pro/) - The commercial side of Root-Me: learning paths and vendor-run events for companies and schools.

### Built for classrooms

- [CyLab Security Academy](https://cylabacademy.org/) - Carnegie Mellon's free platform, formerly picoCTF. Classrooms, assignments, class scoreboards and timed scrimmages, using the Academy's own challenges.
- [Hack The Box for Universities](https://www.hackthebox.com/universities) - Classroom controls, progress reports and syllabus mapping on Hack The Box content.
- [TryHackMe for education](https://tryhackme.com/classrooms) - Curriculum mapping, Moodle and Canvas integration, and uploading your own labs.
- [CTF-Hub for educators](https://ctf-hub.io/for-educators) - Courses and CTF labs with your own content, connected to an LMS over LTI 1.3.

### Archived or dormant

Listed so that nobody builds an event on them by accident.

- [FBCTF](https://github.com/facebookarchive/fbctf) - Archived in 2020. Licensed CC BY-NC 4.0, which is not an open-source software licence.
- [picoCTF platform](https://github.com/CyLabAcademy/picoCTF) - The 2019 platform. Archived in 2024; its own README recommends against using it for new competitions.
- [redpwn/rctf](https://github.com/redpwn/rctf) - The original rCTF repository. Archived in 2025; development continues at otter-sec/rctf.
- [Mellivora](https://github.com/Nakiami/mellivora) - PHP CTF engine. Not archived, but no commits since 2023. GPL-3.0.

## Comparison

| Platform | Kind | Who hosts it | Your own challenges | Per-player or per-team instances | Cost model |
|---|---|---|---|---|---|
| CTF-Hub | Managed multi-tenant platform | Vendor | Yes | Yes, from the Team plan | Free tier, published plans |
| CTFd (open source) | Framework, Apache-2.0 | You | Yes | Through third-party plugins | Free; you pay for servers |
| CTFd (hosted, Enterprise) | Vendor-hosted CTFd | Vendor, or you on Enterprise | Yes | Yes | Published tiers; Enterprise through sales |
| rCTF | Platform, Apache-2.0 | You | Yes | Optional per-team instancer | Free; you pay for servers |
| GZCTF | Platform, AGPL-3.0 core | You | Yes | Built in | Free; you pay for servers |
| RootTheBox | Game-style scoring engine, Apache-2.0 | You | Yes | Not documented | Free; you pay for servers |
| kCTF | Challenge infrastructure, not a scoreboard | You | Yes | Yes, that is its purpose | Free; you pay for the cluster |
| Hack The Box CTF Marketplace | Vendor-hosted event product | Vendor | Vendor content; custom on request | Vendor-run | Through the vendor |
| TryHackMe CTF Builder | Vendor-hosted event product | Vendor | Vendor content; bespoke as a service | Vendor-run | Through the vendor |
| CyLab Security Academy | Free classroom platform | Carnegie Mellon | No, the Academy's challenges | Not documented | Free |

"Not documented" means the project's public pages do not say. It does not mean the feature is missing.

## Which one should you pick?

- **A community or student team running a public weekend CTF, and you already run servers:** self-host [CTFd](https://github.com/CTFd/CTFd) or [rCTF](https://github.com/otter-sec/rctf). Both are proven at scale and cost nothing but infrastructure. Add [kCTF](https://github.com/google/kctf) if you need hardened hosting for remote-exploitation challenges.
- **You want dynamic containers built in and are happy on Docker or Kubernetes:** [GZCTF](https://github.com/GZTimeWalker/GZCTF).
- **A company, university or training team that wants a private, branded event with its own challenges and nothing to install:** [CTF-Hub](https://ctf-hub.io). This is the case it was built for, and it is our recommendation here: isolated per-organisation tenants, container challenges, SSO and LMS integration without running any of it yourself.
- **You love CTFd and just do not want to operate it:** [CTFd's hosted tiers](https://ctfd.io/pricing/).
- **You want an event next week and have no challenges of your own:** [Hack The Box CTF Marketplace](https://www.hackthebox.com/capture-the-flag) or [TryHackMe CTF Builder](https://tryhackme.com/resources/blog/new-ctf-builder), which supply the content.
- **A school class on no budget:** [CyLab Security Academy](https://cylabacademy.org/).
- **Everything must stay on your own infrastructure:** one of the open-source options. CTF-Hub has no self-hosted edition.

## Tools for organisers

- [CTFtime for organisers](https://ctftime.org/for-organizers/) - How to list an event on the community calendar and earn rating points for teams.
- [ctfd-whale](https://github.com/frankli0324/ctfd-whale) - Community plugin that gives self-hosted CTFd per-player Docker instances.
- [rCDS](https://github.com/redpwn/rcds) - Challenge deployment tool recommended by the original rCTF project.
- [nsjail](https://github.com/google/nsjail) - The process sandbox kCTF uses to isolate each connection.

## Play and practise

- [CTFtime](https://ctftime.org/) - The calendar, archive and team ratings for CTF events. Start here to find something to play this weekend.
- [CyLab Security Academy](https://cylabacademy.org/) - Free, beginner-friendly challenges and learning paths.
- [pwn.college](https://pwn.college/) - Arizona State University's free course-like platform for binary exploitation and more.
- [OverTheWire](https://overthewire.org/wargames/) - Classic free wargames, starting with Bandit for shell basics.
- [Hack The Box](https://www.hackthebox.com/) - Large library of machines and challenges.
- [TryHackMe](https://tryhackme.com/) - Guided rooms and learning paths.
- [Root-Me](https://www.root-me.org/) - Long-running community challenge site.
- [PentesterLab](https://pentesterlab.com/) - Web hacking and code review exercises based on real CVEs.
- [LetsDefend](https://letsdefend.io/) - Blue-team practice in a simulated SOC.
- [SANS Holiday Hack Challenge](https://www.sans.org/cyber-ranges/) - Free yearly event from SANS.

## Competitions worth knowing

- [DEF CON CTF](https://defcon.org/) - The best-known finals in the field.
- [Google CTF](https://capturetheflag.withgoogle.com/) - Google's yearly competition.
- [PlaidCTF](https://plaidctf.com/) - Run by Carnegie Mellon's Plaid Parliament of Pwning.
- [CSAW CTF](https://www.csaw.io/) - Student-focused competition from NYU.

The full calendar lives on [CTFtime](https://ctftime.org/event/list/upcoming).

## Other lists

- [apsdehal/awesome-ctf](https://github.com/apsdehal/awesome-ctf) - The classic list of CTF tools and resources.
- [devploit/awesome-ctf-resources](https://github.com/devploit/awesome-ctf-resources) - Tools, platforms and write-ups.

## The egg

A list about Capture The Flag ought to have a flag in it, so this one does.

- The flag looks like `CTFHUB{...}`.
- Three steps. No guessing, no brute force, nothing outside this repository.
- Whoever finds it also finds out what it is worth. It is worth something real.
- The only hint: read​‌‌‌‌​​​​‌‌​‌‌‌‌​‌‌‌​​‌​​​‌​​​​​​‌‌​‌​‌‌​‌‌​​‌​‌​‌‌‌‌​​‌​​‌‌‌​‌​​​‌​​​​​​‌‌‌​​‌‌​‌‌​​​‌‌​‌‌​‌‌‌‌​‌‌‌​​‌​​‌‌​​‌​‌​‌‌​​​‌​​‌‌​‌‌‌‌​‌‌​​​​‌​‌‌‌​​‌​​‌‌​​‌​​​​‌​‌‌‌​​​‌​​​​​​‌‌‌​‌​​​‌‌​‌​​​​‌‌​​‌​‌​​‌​​​​​​‌‌‌​‌​​​‌‌‌​​‌​​‌‌​​‌​‌​‌‌​​‌​‌​​‌​​​​​​‌‌​​‌‌​​‌‌​‌‌‌‌​‌‌‌​​‌​​‌‌​​‌‌‌​‌‌​‌‌‌‌​‌‌‌​‌​​​​‌​​​​​​‌‌​​​​‌​​‌​​​​​​‌‌​​‌‌​​‌‌​‌​​‌​‌‌​‌‌​​​‌‌​​‌​‌​​‌‌‌​‌‌​​‌​​​​​​‌‌​​‌‌‌​‌‌​‌​​‌​‌‌‌​‌​​​​‌​​​​​​‌‌​‌‌​​​‌‌​‌‌‌‌​‌‌​​‌‌‌​​‌​​​​​​‌‌​​‌​​​‌‌​‌​​‌​‌‌​​‌​​​​‌​​​​​​‌‌​‌‌‌​​‌‌​‌‌‌‌​‌‌‌​‌​​​​‌​‌‌‌​ this page more literally than a browser does.

Please do not post the flag in issues or pull requests.

## Contributing

Pull requests are welcome, including ones that correct an entry about CTF-Hub or a competitor. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related rights to this list.
