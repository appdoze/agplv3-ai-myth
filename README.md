# 🕵️ The AGPLv3 AI Myth — A Case Study in Misread Licenses

> *"LLM generated code cannot be submitted to Peacock as it violates AGPLv3"*
> — A claim made with full confidence and zero legal basis.

This repository documents, fact-checks, and debunks the claim that the **GNU Affero General Public License v3 (AGPLv3)** prohibits the use of AI/LLM tools in open source contributions — using the [Peacock project](https://github.com/thepeacockproject/Peacock) as the case study.

No lawyers were harmed in the making of this repository. No Peacock maintainers were named or targeted personally. This is purely an educational resource about open source licensing and AI policy.

---

## 📋 Table of Contents

1. [The Claim](#-the-claim)
2. [The Evidence Examined](#-the-evidence-examined)
3. [What AGPLv3 Actually Says](#-what-agplv3-actually-says)
4. [Peacock's Repository — A Full Audit](#-peacocks-repository--a-full-audit)
5. [The Arguments Made & Why They Fail](#-the-arguments-made--why-they-fail)
6. [How To Actually Ban AI Contributions (If You Want To)](#-how-to-actually-ban-ai-contributions-if-you-want-to)
7. [Verdict](#-verdict)
8. [Further Reading](#-further-reading)

---

## 🎯 The Claim

A contributor to the Peacock project was told:

> *"LLM generated code cannot be submitted to Peacock as it violates AGPLv3"*

When challenged, the claim was doubled down on with:

> *"It doesn't need to literally mention it, there's probably no country that explicitly bans feeding someone to a hippo, but you're still murdering someone which is illegal everywhere."*

And further:

> *"Feel free to prove me wrong with an actual lawyer."*

And:

> *"I'm not aware of any legal reasons why a contribution policy would matter."*

Let's go through each of these claims methodically.

---

## 🔍 The Evidence Examined

### Files audited in the Peacock repository

| File | Exists? | Mentions AI/LLM? |
|------|---------|-----------------|
| `LICENSE` | ✅ Yes (AGPLv3) | ❌ No |
| `docs/CODE_OF_CONDUCT.md` | ✅ Yes (Contributor Covenant v2.0 boilerplate) | ❌ No |
| `.github/pull_request_template.md` | ✅ Yes | ❌ No |
| `CONTRIBUTING.md` | ❌ Does not exist | N/A |
| `readme.md` | ✅ Yes | ❌ No |
| Issues/PRs mentioning AI | ❌ Zero results | N/A |
| Code search: "AI", "LLM", "ChatGPT", "Copilot", "generated" | ❌ Zero results | N/A |

**Result: There is no documented rule anywhere in the Peacock repository prohibiting AI-generated contributions.**

---

## 📜 What AGPLv3 Actually Says

The full AGPLv3 license is available at https://www.gnu.org/licenses/agpl-3.0.en.html

AGPLv3 concerns itself with exactly **one thing**: how you **distribute** and **modify** software. Specifically:

- If you distribute the software → you must provide source code under AGPLv3
- If you run a modified version on a network server → you must provide source to users of that server
- If someone modifies the software for you → they must do so under your direction and not keep copies outside that relationship

### What AGPLv3 does NOT say

| Topic | Mentioned in AGPLv3? |
|-------|---------------------|
| How code must be written | ❌ |
| What tools contributors may use | ❌ |
| Whether AI/LLM assistance is permitted | ❌ |
| Authorship requirements | ❌ |
| "Original" work requirements | ❌ |
| Contribution policies | ❌ |

The word **"original"** does not appear in AGPLv3 in any authorship context. The license does not care if your code was written by a human, an AI, or a cat walking across a keyboard — as long as distribution obligations are met.

---

## 🔬 The Arguments Made & Why They Fail

### Argument 1: "It violates AGPLv3"

**Claim:** Using LLM-generated code in contributions violates AGPLv3.

**Reality:** AGPLv3 governs *distribution*, not *authorship*. There is no clause — direct or implied — that regulates how contributed code is written. This is not a close call or a grey area. It is straightforwardly incorrect.

**Verdict: ❌ False**

---

### Argument 2: "It doesn't need to literally mention it" (the hippo analogy)

**Claim:** Just like no country needs to explicitly ban feeding someone to a hippo for it to be murder, AGPLv3 doesn't need to explicitly mention AI for it to be prohibited.

**Why this fails:** The hippo analogy works because feeding someone to a hippo *maps directly onto an existing law* (homicide). The underlying prohibited act (killing a person) IS in the law — the method doesn't matter.

For this analogy to hold for AI code, you'd need to show that using an LLM maps onto an *existing AGPLv3 clause*. There is no such clause. It's not a novel method of doing something already prohibited. It's something the license simply never addresses.

A more accurate analogy:
> "You can't write code with a blue pen for this project" — "why?" — "well the law doesn't need to explicitly mention blue pens..."

There is no underlying prohibition being triggered here.

**Verdict: ❌ Analogy fails**

---

### Argument 3: "Contribution policies don't matter legally"

**Claim:** A CONTRIBUTING.md would have no legal weight, unlike a license.

**Reality:** Contribution policies have significant legal precedent:

- **Developer Certificate of Origin (DCO)** — used by the Linux kernel, not a license, legally meaningful in court
- **Contributor License Agreements (CLAs)** — pure policy documents, routinely upheld by courts
- **GitHub Terms of Service** — a policy document, not legislation, legally enforceable
- Employment contracts, NDAs, and codes of conduct are all "policy documents" with legal force

A properly worded CONTRIBUTING.md requiring contributors to certify their code is not AI-generated would be **more targeted and more enforceable** for this specific goal than stretching a distribution license to cover something it was never designed for.

**Verdict: ❌ Incorrect**

---

### Argument 4: "The license applies to forks, a policy document doesn't"

**Claim:** Because AGPLv3 is legally binding and applies to forks, it's more powerful than a contribution policy.

**What they got right:** ✅ AGPLv3 is legally binding. ✅ It applies to forks. ✅ Relicensing past contributions requires contributor consent.

**What they missed:** Even if AGPLv3 applied to forks perfectly — it still doesn't ban AI code, because it never did. A fork is equally free to accept AI contributions under AGPLv3 because the license never prohibited it. You cannot use a license to enforce something the license doesn't say.

**Verdict: ⚠️ Partially correct premises, incorrect conclusion**

---

## 🛠️ How To Actually Ban AI Contributions (If You Want To)

If a project genuinely wants to prohibit AI-generated contributions, here's how to do it **correctly and legally**:

### Option 1: Add a CONTRIBUTING.md (simplest, immediate)

```markdown
## AI-Generated Code Policy

Contributions generated in whole or in part by AI language models (including
but not limited to ChatGPT, GitHub Copilot, Claude, Gemini, etc.) are not
accepted in this project. By submitting a pull request, you certify that your
contribution was written by a human author.
```

This is a clear, enforceable project rule. No license change needed.

### Option 2: Add a CLA (Contributor License Agreement)

A CLA can include a clause like:

> *"Contributor certifies that the submitted code was not generated by an AI language model."*

CLAs are legally binding documents with real case law behind them. Far more enforceable than misinterpreting a license.

### Option 3: Add DCO-style sign-off requirement

Similar to the Linux kernel's approach — require a sign-off line in every commit:

```
Signed-off-by: Your Name <email>
No-AI-Generated: true
```

### Option 4: Custom License (nuclear option)

Write a custom license that explicitly prohibits AI contributions. **Downside:** This immediately makes the project non-open-source by OSI definition, since OSI does not approve licenses with arbitrary contribution restrictions. The project would need to stop calling itself "open source."

### ⚠️ What NOT to do

Don't claim AGPLv3 prohibits it when it doesn't. It:
- Misleads contributors
- Creates a false chilling effect
- Is legally inaccurate
- Damages the project's credibility on licensing matters

---

## ⚖️ Verdict

| Claim | Verdict |
|-------|---------|
| "AGPLv3 prohibits AI-generated contributions" | ❌ False |
| "It doesn't need to explicitly say it" | ❌ The hippo analogy requires an underlying law being broken — there is none here |
| "Contribution policies have no legal weight" | ❌ False — DCO, CLAs, and ToS documents are all legally meaningful |
| "There is a written AI policy in Peacock's repo" | ❌ False — zero mentions across all files |
| "The license applies to forks so it matters more" | ⚠️ True but irrelevant — the license still doesn't say what they claim |

**Summary:** The project has a legitimate *preference* against AI-generated code. That preference is entirely valid for maintainers to hold. However, it has not been documented anywhere, and the legal justification given (AGPLv3) is incorrect. The fix is simple: write a `CONTRIBUTING.md`. The license is not the right tool for this job.

---

## 📚 Further Reading

- [GNU AGPLv3 Full Text](https://www.gnu.org/licenses/agpl-3.0.en.html)
- [Linux Kernel DCO](https://developercertificate.org/)
- [What is a CLA and why does it matter?](https://opensource.com/article/18/3/cla-vs-dco-whats-difference)
- [Contributor Covenant (CoC used by Peacock)](https://www.contributor-covenant.org/version/2/0/code_of_conduct/)
- [OSI Open Source Definition](https://opensource.org/osd)
- [GitHub's guide to writing a CONTRIBUTING.md](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)

---

## ⚠️ Disclaimer

This repository is an educational resource about open source licensing. It is not legal advice. It does not target or harass any individual. The Peacock project maintainers have every right to set their own contribution policies — this document simply argues they should write them down accurately rather than citing an incorrect legal basis.

---

*Made with 🔍 detective energy and zero hippos.*
