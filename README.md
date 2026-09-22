# Rafeeq Mini — رفيق المصغّر

### Bilingual Agentic AI Delivery-Support Agent · وكيل ذكاء اصطناعي توكيلي ثنائي اللغة لدعم عمليات التوصيل

**Advanced Agentic AI Systems Engineering — SDAIA Academy** · دورة هندسة أنظمة الذكاء الاصطناعي التوكيلي المتقدمة — أكاديمية سدايا

---

## 📌 Overview · نظرة عامة

**English:** Rafeeq Mini is a bilingual agentic operations assistant for a fictional delivery company, built as the cumulative capstone of the **Advanced Agentic AI Systems Engineering** course at **SDAIA Academy**. It understands an Arabic or English order/refund request, verifies the supplied synthetic customer scope, retrieves the active policy, routes the task to a specialist agent, and pauses any simulated refund above **SAR 500** for documented human approval.

**العربية:** رفيق المصغّر مساعد عمليات وكيلي ثنائي اللغة لشركة توصيل افتراضية، بُني كمشروع ختامي تراكمي ضمن دورة **هندسة أنظمة الذكاء الاصطناعي التوكيلي المتقدمة** في **أكاديمية سدايا**. يفهم طلبًا بالعربية أو الإنجليزية عن طلب شراء أو استرداد، ويتحقق من نطاق العميل المصطنع، ويسترجع السياسة السارية، ويوجه المهمة إلى وكيل متخصص، ويوقف الاسترداد المحاكى الأعلى من **500 ريال** حتى توثيق الموافقة البشرية.

> ⚠️ **Safety boundary · حد الأمان:** This is a synthetic training simulation. It does not contact any real delivery, payment, or customer system. No real customer, payment, order, or enterprise data is used. · هذه محاكاة تدريبية ببيانات اصطناعية ولا تتصل بأي نظام توصيل أو دفع أو عملاء حقيقي.

---

## 🎯 Project Objectives · أهداف المشروع

| # | Objective · الهدف |
|---|---|
| 1 | Design a bounded agentic architecture with typed state and a bounded transition graph. · تصميم معمارية وكيلية محدودة بحالة محددة النوع ومخطط انتقالات محدود. |
| 2 | Implement tool calling with strict schemas and a local MCP server/client. · تنفيذ استدعاء الأدوات بمخططات صارمة وخادم/عميل MCP محلي. |
| 3 | Add session memory, scoped recall, and policy retrieval (RAG over synthetic policy chunks). · إضافة ذاكرة جلسة واسترجاع معزول وسحب سياسات. |
| 4 | Coordinate specialist agents with typed delegation and a supervisor. · تنسيق وكلاء متخصصين بتفويض محدد النوع تحت إشراف منسق. |
| 5 | Enforce a human-approval interrupt for simulated refunds above SAR 500. · فرض إيقاف للموافقة البشرية على الاستردادات المحاكاة الأعلى من 500 ريال. |
| 6 | Threat-model, attack, fix, retest, and evaluate traces before a safe export. · نمذجة التهديدات والهجوم والإصلاح وإعادة الفحص وتقييم الأثر قبل التصدير الآمن. |

---

## 🗓️ Three-Day Cumulative Build · البناء التراكمي خلال ثلاثة أيام

The project is built progressively through **30 cells (C0–C29)** and **14 guided learner exercises (TODO-1 … TODO-14)** in a single Google Colab notebook. · يُبنى المشروع تدريجيًا عبر **30 خلية (C0–C29)** و **14 تمرينًا موجهًا** في دفتر كولاب واحد.

| Day · اليوم | Cells · الخلايا | Build outcome · ناتج البناء | Gate · البوابة |
|---|---|---|---|
| **Day 1 · اليوم الأول** | `C0–C9` | Environment doctor, architecture, typed state, bounded graph, observable traces, ReAct loop, tool schema, local MCP server/client. · فاحص البيئة والمعمارية والحالة المحددة والمخطط المحدود والتتبع المرصود وحلقة ReAct ومخطط الأداة وخادم/عميل MCP. | `C9_DAY1_GATE` ✅ |
| **Day 2 · اليوم الثاني** | `C10–C20` | State restore, session memory, scoped recall, policy retrieval, specialist agents, supervisor, typed delegation, Plan-and-Execute, interrupt/resume approval. · استعادة الحالة وذاكرة الجلسة والاسترجاع المعزول وسحب السياسات والوكلاء المتخصصين والمنسق والتفويض المحدد وPlan-and-Execute وإيقاف/استئناف الموافقة. | `C20_DAY2_GATE` ✅ |
| **Day 3 · اليوم الثالث** | `C21–C29` | Threat model, attack suite, guard fix/retest, reflection gate, trace evaluation, one measured optimization, scorecard, readiness, and safe export. · نموذج التهديد وحزمة الهجوم وإصلاح الحارس وإعادة الفحص وبوابة المراجعة وتقييم الأثر وتحسين واحد مقاس وبطاقة الأداء والجاهزية والتصدير الآمن. | `C29_EXPORT_SAFETY_CHECK` ✅ |

---

## ✅ Final Results · النتائج النهائية

All critical gates and learner checks passed on Colab Free CPU with `LLM_MODE=stub`:

| Check · الفحص | Result · النتيجة |
|---|---|
| Functional cases (AR + EN) · الحالات الوظيفية | ✅ Pass |
| Security / attack cases · حالات الأمان والهجوم | ✅ Pass |
| Risk flags exact · علامات الخطورة الدقيقة | ✅ Pass |
| Cross-customer leakage = 0 · تسرب بيانات بين العملاء | ✅ Zero |
| Unauthorized writes = 0 · كتابات غير مصرح بها | ✅ Zero |
| Human approval above SAR 500 · الموافقة البشرية فوق 500 ريال | ✅ Enforced |
| No write retries · عدم إعادة محاولة الكتابة | ✅ Pass |
| Bounded termination · إنهاء محدود | ✅ Pass |
| Trace redacted (no PII / chain-of-thought) · أثر منقح | ✅ Pass |
| One measured safe optimization · تحسين واحد مقاس وآمن | ✅ Pass |
| Public tests · الاختبارات العامة | ✅ Pass |
| Learner exercises TODO-11 → TODO-14 · تمارين المتدرب | ✅ All True |

📄 Machine-readable evidence: `reports/assessment_results.json` · Human-readable reports: `reports/PROJECT_REPORT.md` and `reports/SECURITY_ASSESSMENT.md`

---

## 🧠 Architecture · المعمارية

```
┌─────────────────────────────────────────────────────────────┐
│  User Request (AR / EN) · طلب المستخدم                       │
│  "refund order ORD-1001" / "أريد استرداد الطلب"               │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│  Supervisor Agent · وكيل المنسق                               │
│  Bounded graph · typed state · step/transition limits         │
└───────┬───────────────────────┬───────────────────────┬───────┘
        ▼                       ▼                       ▼
┌───────────────┐      ┌──────────────────┐      ┌──────────────────┐
│ Order Lookup  │      │ Policy Retrieval │      │ Refund Writer    │
│ Agent         │      │ Agent (RAG over  │      │ Agent            │
│ · MCP tools   │      │ synthetic chunks)│      │ · interrupt for  │
│ · typed state │      │ · scoped recall  │      │   SAR 500+       │
└───────────────┘      └──────────────────┘      └────────┬─────────┘
                                                          ▼
                                              ┌──────────────────────┐
                                              │ Human Approval Gate  │
                                              │ بوابة الموافقة البشرية│
                                              └──────────────────────┘
```

**Design principles · مبادئ التصميم:**

- **Bounded runtime** — hard limits on steps, transitions, handoffs, and reflections guarantee termination. · حدود صارمة على الخطوات والانتقالات والتفويضات والمراجعات تضمن الإنهاء.
- **Typed, scoped state** — customer identity and approvals live *outside* model-controlled arguments. · هوية العميل والموافقات خارج وسائط النموذج.
- **Deterministic stub LLM** — `LLM_MODE=stub` keeps every run reproducible with no API key and no network. · نموذج Stub حتمي يجعل كل تشغيل قابلًا لإعادة الإنتاج دون مفتاح API أو شبكة.
- **Observable traces** — every decision logs decision, tool, route, result, and counters (no private chain-of-thought). · أثر مرصود لكل قرار دون تخزين التفكير الداخلي.
- **Secure by default** — redacted traces, zero cross-customer leakage, zero unauthorized writes. · آمن افتراضيًا بأثر منقح وصفر تسرب وصفر كتابات غير مصرح بها.

---

## 🛠️ Tech Stack · التقنيات

- **Runtime:** Google Colab Free CPU (no GPU required) · بيئة تشغيل كولاب المجانية
- **Language:** Python (standard library only for the agent core) · بايثون بمكتبتها القياسية للنواة
- **Model:** Deterministic `LLM_MODE=stub` · نموذج حتمي غير متصل
- **Visualization:** Matplotlib (with built-in fallback) · مرئيات اختيارية مع بديل مضمّن
- **Protocol:** Model Context Protocol (MCP) server/client, local · بروتوكول MCP محلي
- **Patterns:** ReAct · Plan-and-Execute · Supervisor + Specialist agents · Reflection gate · Interrupt/Resume approval

---

## 📂 Repository Structure · بنية المستودع

```
Rafeeq_AyshaAljaafari_AdvancedAgenticAISystemsEngineering/
├── LEARNING_PROGRESS.md              # Safe public progress log · سجل التقدم الآمن
├── README.md                         # This file · هذا الملف
├── notebooks/
│   └── Rafeeq_Mini_Capstone.ipynb    # Final notebook, cells C0–C29 · الدفتر النهائي
├── data/                             # Synthetic public data · بيانات مصطنعة عامة
├── src/                              # Agent core modules · وحدات نواة الوكيل
├── mcp_server/                       # Local MCP server/client · خادم/عميل MCP
├── tests/                            # Public checks · الفحوص العامة
├── reports/
│   ├── PROJECT_REPORT.md             # Generated by C28_READINESS
│   ├── SECURITY_ASSESSMENT.md        # Generated by C23_GUARD_FIX_RETEST
│   ├── EVIDENCE_CARD.md              # One concise card per day (learner) · بطاقة أدلة لكل يوم
│   ├── trace.jsonl                   # Sanitized trace (C25) · أثر منقح
│   ├── assessment_results.json       # Scorecard (C27) · نتائج التقييم
│   ├── monitoring_dashboard.png      # Dashboard (C27) · لوحة المراقبة
│   └── submission_manifest.json      # C29 export manifest · بيان التسليم
└── .github/workflows/                # Learner submission quality check · فحص التسليم الآلي
```

---

## ▶️ How to Run · طريقة التشغيل

1. Open `https://colab.research.google.com/github/almiyead-rgb/rafeeq-agentic-ai-labs/blob/v0.9.0-rc3/notebooks/Rafeeq_Mini_Capstone.ipynb` in **Google Colab** (standard CPU runtime; no GPU needed). · افتح الدفتر في كولاب ببيئة CPU القياسية.
2. Run all cells **from top to bottom** (`C0 → C29`); do not skip dependencies. · شغّل الخلايا من الأعلى إلى الأسفل دون تخطي الاعتماديات.
3. Complete only the numbered learner exercises (`TODO-1 … TODO-14`) when prompted. · أكمل تمارين المتدرب المرقمة فقط.
4. Day gates: `C9_DAY1_GATE` and `C20_DAY2_GATE` must print `all_passed=true`. · يجب أن تطبع بوابتا اليومين الأول والثاني `all_passed=true`.
5. Enable the `FINAL_EXPORT` switch and rerun `C29_EXPORT_SAFETY_CHECK` — it must print `FINAL_EXPORT_CREATED`. · فعّل مفتاح التصدير النهائي وأعد تشغيل C29 حتى يطبع `FINAL_EXPORT_CREATED`.

> 🔁 If the Colab runtime resets: reopen your Drive copy, run `C0_ENV_DOCTOR`, then rerun completed cells from the top. · إذا أُعيد ضبط بيئة كولاب: افتح النسخة المحفوظة وشغّل فاحص البيئة ثم أعد الخلايا من الأعلى.

---

## 📚 Technical Documentation · التوثيق الفني

| Document · الوثيقة | Location · الموقع | Content · المحتوى |
|---|---|---|
| Project report · تقرير المشروع | [`reports/PROJECT_REPORT.md`](reports/PROJECT_REPORT.md) | Architecture, gates, measured optimization, readiness · المعمارية والبوابات والتحسين المقاس والجاهزية |
| Security assessment · التقييم الأمني | [`reports/SECURITY_ASSESSMENT.md`](reports/SECURITY_ASSESSMENT.md) | Threat model, attack suite, guard fix and retest · نموذج التهديد وحزمة الهجوم وإصلاح الحارس وإعادة الفحص |
| Learning progress · سجل التقدم | [`LEARNING_PROGRESS.md`](LEARNING_PROGRESS.md) | Safe public checkpoints: setup, Day 1, Day 2, Day 3 · نقاط التقدم العامة الآمنة |
| Notebook docs · توثيق الدفتر | [`notebooks/`](notebooks/) | Final capstone notebook C0–C29 · دفتر التسليم النهائي |
| Agent core · نواة الوكيل | [`src/`](src/) | Typed state, bounded graph, agents · الحالة المحددة والمخطط المحدود والوكلاء |
| MCP integration · تكامل MCP | [`mcp_server/`](mcp_server/) | Local MCP server/client · خادم/عميل MCP المحلي |
| Public checks · الفحوص العامة | [`tests/`](tests/) | Validated public test suite · الاختبارات العامة المتحقق منها |
| Learner guide · دليل المتدرب | [almiyead-rgb/rafeeq-agentic-ai-labs](https://github.com/almiyead-rgb/rafeeq-agentic-ai-labs) | Official course guide used for this build · دليل الدورة الرسمي المتبع في البناء |

---

## 📊 Evidence & Reports · الأدلة والتقارير

Every important claim maps to a cell, a public synthetic case, and its result:

| Artifact · الملف | Produced by · توليده | Content · المحتوى |
|---|---|---|
| `reports/PROJECT_REPORT.md` | `C28_READINESS` | Architecture, gates, optimization, readiness · التقرير الفني |
| `reports/SECURITY_ASSESSMENT.md` | `C23_GUARD_FIX_RETEST` | Threat model, attack suite, fix + retest · التقييم الأمني |
| `reports/trace.jsonl` | `C25` | Sanitized decision trace · الأثر المنقح |
| `reports/assessment_results.json` | `C27` | Machine-readable scorecard · النتائج |
| `reports/monitoring_dashboard.png` | `C27` | Visual scorecard · لوحة المراقبة |
| `reports/EVIDENCE_CARD.md` | Learner (post-export) | One concise evidence card per day · بطاقة أدلة |

---

## 🛡️ Privacy, Identity & Academic Integrity · الخصوصية والهوية والنزاهة الأكاديمية

- Only the synthetic `learner_id` / GitHub username appears in public files; real identity is submitted exclusively through the instructor's private hand-in form. · لا يظهر في الملفات العامة سوى المعرف الاصطناعي أو اسم مستخدم GitHub، وتُرسل الهوية الحقيقية عبر نموذج التسليم الخاص فقط.
- No credentials, tokens, API keys, private links, real customer data, or private chain-of-thought are published. · لا تُنشر بيانات دخول أو مفاتيح أو روابط خاصة أو بيانات عملاء حقيقية أو تفكير داخلي.
- Only learner `TODO` areas were completed; official source cells, public tests, and validators were not modified. · أكملت مناطق المتدرب فقط دون تعديل المصدر الرسمي أو الاختبارات العامة.
- Course materials are reused under the limited `COURSE_USE_PERMISSION.md`. · إعادة استخدام مواد الدورة خاضعة لإذن الاستخدام المحدود.

---

## 🙏 Acknowledgments · الشكر والتقدير

- **SDAIA Academy · أكاديمية سدايا:** [github.com/SDAIAAcademy](https://github.com/SDAIAAcademy) — the official SDAIA Academy GitHub organization for the training program. · المنظمة الرسمية لأكاديمية سدايا على GitHub لبرامجها التدريبية: https://github.com/SDAIAAcademy
- **Training program · البرنامج التدريبي:** Advanced Agentic AI Systems Engineering course · دورة هندسة أنظمة الذكاء الاصطناعي التوكيلي المتقدمة — [sdaia.gov.sa](https://sdaia.gov.sa)
- **Course Trainer · المدربة:** Meaad Al-Marri · ميعاد المري
- **Official course repository · مستودع الدورة الرسمي:** [almiyead-rgb/rafeeq-agentic-ai-labs](https://github.com/almiyead-rgb/rafeeq-agentic-ai-labs) — the starting notebook and learner guide live there; this repository is a standalone learner submission, not a fork. · مستودع الدورة الرسمي هو نقطة البداية، وهذا المستودع تسليم مستقل للمتدربة وليس Fork.
- **Working notebook copy · نسخة الدفتر العاملة:** Google Colab

---

## 📬 Hand-in · التسليم

- Final commit recorded via the instructor's private hand-in form (repository URL + final commit SHA + the three gate markers). · Commit النهائي مسجل في نموذج التسليم الخاص مع رابط المستودع وعلامات البوابات الثلاث.
- Automated validation: **Actions → Learner submission quality** is green for the final commit. · التحقق الآلي عبر Actions ناجح لنفس Commit التسليم.
- This is an educational training project — not a production deployment. · مشروع تدريبي تعليمي وليس نشرًا إنتاجيًا.

---

**Built with a bounded, observable, and safe-by-default agentic architecture.** · **بُني بمعمارية وكيلية محدودة ومرصودة وآمنة افتراضيًا.**

---

## ✅ SDAIA Administrative Requirements — 10 Points · متطلبات سدايا الإدارية — 10 درجات

| Required evidence · الدليل المطلوب | Where it is satisfied · موقع تحقيقه في هذا المستودع |
|---|---|
| Clear, comprehensive GitHub repository description (2 pts) · وصف واضح وشامل لمستودع GitHub | Repository **About** description + this README · وصف About + هذا الملف |
| Professional README: idea, run, and use (2 pts) · README احترافي: الفكرة والتشغيل والاستخدام | [Overview](#-overview--نظرة-عامة) · [How to Run](#️-how-to-run--طريقة-التشغيل) · [Architecture](#-architecture--المعمارية) |
| Appropriate linked technical documentation (2 pts) · توثيق فني مناسب ومترابط | [Technical Documentation](#-technical-documentation--التوثيق-الفني) with linked reports, source, tests, and learner guide · جدول التوثيق الفني المترابط |
| Safe, meaningful Git progress and version history (2 pts) · تقدم Git آمن وذو معنى وسجل إصدارات محفوظ | [`LEARNING_PROGRESS.md`](LEARNING_PROGRESS.md) + documented commit messages (`docs:`, `feat:`) · سجل التقدم الآمن ورسائل Commits موثقة |
| Training-program reference in README (1 pt) · الإشارة إلى البرنامج التدريبي في README | [Acknowledgments](#-acknowledgments--الشكر-والتقدير): SDAIA Academy + course name · قسم الشكر والتقدير |
| Working SDAIA Academy GitHub link (1 pt) · رابط أكاديمية سدايا الصحيح | [github.com/SDAIAAcademy](https://github.com/SDAIAAcademy) in Acknowledgments · الرابط في قسم الشكر |


