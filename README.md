# FlyRank ML Internship — Starter Repo

**Applied Search Intelligence: Google Search Ranking & Discoverability**

This is the starting point for the FlyRank ML Internship. You **clone it into your own public
repo** (one click — *Use this template*), build everything there, and submit that repo URL on
each assignment in your portal — it's your workspace, your submission, and your portfolio all
at once. The rhythm is simple: do the work, commit it, submit on the card. Done.

Everything here runs on a small **anonymized** slice of real FlyRank search data. No credentials,
no private client data, no setup headaches.

> **New here?** Two reads: **[SETUP.md](SETUP.md)** (GitHub, Colab, and data access — ten
> minutes, with every silent pitfall flagged), then **[GUIDE.md](GUIDE.md)** (every file
> explained, what to edit vs. leave alone, and where your own work goes — five minutes).

---

## Quickstart — first win in 2 minutes

The fastest path is Google Colab (one click, zero install). Open Notebook 1 and run all cells:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/notebooks/01_first_look_and_discovery.ipynb)
 **Week 1 — Run it, then discover a real truth yourself**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/notebooks/02_your_first_readable_model.ipynb)
 **Week 2 — The model is just a rule you can read**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/notebooks/03_working_with_the_full_release.ipynb)
 **Weeks 3+ — The full release (~79M rows) via DuckDB, no download needed** — hosted at
 [`FlyRank/internship-warehouse`](https://huggingface.co/datasets/FlyRank/internship-warehouse) (gated: request access + accept the data-use terms, approval is instant)

---

## Your assignment notebooks — open, fill, save, done

Every assignment is one pre-named skeleton notebook in `work/notebooks/`. Click its badge,
fill the sections in order, then **File → Save a copy in GitHub → OK** — the dialog is
already pre-filled with your repo and the right path.

> **The badges know whose repo they're in.** About 30 seconds after you create your copy, an
> automatic commit ("Point Colab badges at this copy") rewires every badge in it to open
> **your** notebooks — with your saved work — instead of the shared read-only ones. Reading
> this on the shared starter page? The badges below open blank previews; make your copy
> first ([SETUP.md](SETUP.md), Moment 1).

| Week | Card | Notebook | Open |
|---|---|---|---|
| 1 | ML-02 | `w01_research_question` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w01_research_question.ipynb) |
| 2 | ML-03 | `w02_ml_task_framing` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w02_ml_task_framing.ipynb) |
| 3 | ML-04 | `w03_data_contract` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w03_data_contract.ipynb) |
| 3 | ML-05 | `w03_feature_leakage_check` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w03_feature_leakage_check.ipynb) |
| 4 | ML-06 | `w04_signal_audit` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w04_signal_audit.ipynb) |
| 4 | ML-07 | `w04_baseline_score` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w04_baseline_score.ipynb) |
| 5 | ML-08 | `w05_model` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w05_model.ipynb) |
| 6 | ML-09 | `w06_validation_audit` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w06_validation_audit.ipynb) |
| 7 | ML-10 | `w07_action_playbook` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/w07_action_playbook.ipynb) |
| 8 | ML-11 | `capstone` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/piasa19/flyrank-ml-internship-starter/blob/main/work/notebooks/capstone.ipynb) |

Badges not opening *your* copy? Colab's built-in opener always works: **File → Open notebook
→ GitHub tab** → paste `github.com/you/your-repo` → pick the notebook.

### Prefer local?

```bash
git clone <this-repo-url>
cd flyrank-ml-internship-starter
pip install -r requirements.txt          # or: uv pip install -r requirements.txt
python scripts/run_all.py
```

That runs the whole pipeline on the bundled sample and writes results to `outputs/`.

---

## What you get

| Path | What it is |
|---|---|
| `notebooks/` | Week 1–2 **first-win notebooks** (Colab-ready). Start here. |
| `scripts/01–05` + `run_all.py` | The runnable reference pipeline: prepare → baseline → train → evaluate → PDF. |
| `data/raw/content_refresh_anonymized.csv` | The anonymized starter dataset (~30k pages). |
| `outputs/` | Example outputs so you can see the **target shape** (`model_report.md`, `refresh_queue_sample.csv`, `charts/`). |
| `work/` | **Your space.** Lane experiments and your capstone live here — see `work/README.md`. |
| `docs/` | The core docs + the data dictionary (see below). |

### Read these (in `docs/`)

1. **`ml-core-foundation-framework.md`** — the first-principles map of ML as a whole system. The backbone of the live sessions.
2. **`ml-intern-dataset-and-lane-guide.md`** — how to use the data safely, the capstone workflow, and the analysis "lanes" you can pick from.
3. **`intern-free-tooling-guide.md`** — the zero-budget tool stack (Python, Colab, free AI assistants). You never need to pay for anything.
4. **`data-dictionary.md`** — all 44 columns: meaning, scale, and gotchas. Keep it open while you work.

---

## The pipeline (what `run_all.py` does)

```text
01_prepare_features.py   clean + build the feature vector, define the label
02_baseline_score.py     a transparent hand-rule "fix this first" score
03_train_model.py        logistic regression, decision tree, random forest (client-holdout split)
04_evaluate_and_export.py  ranked queue + charts + Markdown report
05_build_pdf_report.py   a shareable PDF summary
```

On the bundled sample, the learned model clearly beats the hand-written rule at picking the right
pages to review first (**Precision@50 ≈ 0.24 → 0.74**; the model number can land 0.68–0.74
depending on library versions — the ~3x lift is the point). The notebooks compute these numbers
live, so they always reflect the current data and environment.

**Teaching point:** the model is the capstone, but the *workflow* is the lesson —
`problem framing → data cleaning → baseline → first model → evaluation → explainable recommendation`.

---

## Data safety (read `DATA_USE.md`)

- Only the small **anonymized** CSV ships here — no client names, domains, URLs, titles, or keywords.
- **Never** add raw private client data to this repo or your fork. Need more data? Request an approved
  release from your mentor — never export it yourself.
- Don't paste client data into third-party AI tools.
- Frame every result as **observed / measured / directional / decision-support** — never
  "I predicted Google's algorithm."

The `.gitignore` blocks datasets by default, and CI fails any commit that includes a dataset.

---

## Assignments & schedule

Weekly assignments, live events, and the capstone live on **your portal board** (your
enrollment email has your access link). This repo is the shared technical foundation they all
build on — and the `skills/` folder here is the instruction library for your AI assistant
(start at [skills/README.md](skills/README.md)).

**First time with GitHub?** You need exactly four things (full walkthrough: [SETUP.md](SETUP.md)):
1. A free account at github.com.
2. Your own copy of this repo: **Use this template → Create a new repository** → public.
   (One click — brings the notebooks, `work/`, and the CI leak-guard with it.)
3. In Colab: *File → Save a copy in GitHub* — opened from your copy's badges, the dialog is
   already pre-filled with your repo and path, so it's just OK (Colab handles auth).
4. That's your submission repo — share its **github.com/you/your-repo** URL with Assignment 1
   (never a colab.research.google.com or drive.google.com link).

---

*Track leads: Mirza Ašćerić (ML) · Hole (data engineering). Code under MIT (see `LICENSE`); data under `DATA_USE.md`.*

# Content Refresh Prioritization Using Machine Learning

**Author:** Piasa Das  
**Role:** Machine Learning Engineering Intern  
**Organization:** FlyRank AI  
**Project Track:** General AI Fluency  
**Lane:** Refresh / Content Opportunity Scoring

---

## 1. Project Overview

This project focuses on identifying web pages that may need content updates or improvements.

Websites contain many pages, and it can be difficult for editors to decide which pages should be reviewed first.

This project uses data analysis and machine learning to prioritize content pages based on signals such as content age, impressions, clicks, engagement, and performance trends.

The goal is to create a ranked list of pages that can help content teams make better review decisions.

## 2. Who Is This Project For?

This project is designed for:

- Content teams
- SEO analysts
- Digital marketers
- Website managers
- Data analysts

It helps them identify potentially declining content and prioritize pages for human review.

## 3. Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Machine Learning
- GitHub

## 4. Project Workflow

The project follows these main steps:

1. Data Understanding – Exploring the anonymized content dataset.
2. Data Cleaning – Preparing the data for analysis.
3. Feature Engineering – Selecting useful features for the model.
4. Baseline Development – Creating a rule-based prioritization approach.
5. Model Development – Training and comparing machine learning models.
6. Model Evaluation – Evaluating performance using appropriate metrics.
7. Validation Audit – Checking possible data leakage and validation reliability.
8. Recommendations – Using model results to support content review decisions.

## 5. Architecture

```text
Anonymized Content Dataset
          |
          v
     Data Cleaning
          |
          v
   Feature Engineering
          |
          v
   Baseline Prioritization
          |
          v
   Machine Learning Model
          |
          v
    Model Evaluation
          |
          v
   Validation and Audit
          |
          v
 Ranked Content Review List
          |
          v
     Human Review
```

## 6. Model Evaluation (V2)

The project explored machine learning models for content prioritization.

The improved V2 Random Forest model was evaluated after removing potentially leaked features and using client-grouped validation.

**V2 Results:**

| Evaluation Metric | Result |
|---|---:|
| ROC AUC | 0.903 |
| Precision@50 | 0.928 |

These results indicate that the model showed strong ranking and classification performance on the evaluated dataset.

Precision@50 measures the proportion of relevant positive examples among the top 50 prioritized pages.

The results should be interpreted within the scope of the available anonymized dataset and its proxy target.

They do not guarantee that refreshing a page will improve its future performance.

## 7. Data Safety and Leakage Prevention

Data leakage was an important consideration during model development.

The project included:

- Reviewing features for possible target leakage.
- Removing potentially leaked features.
- Using client-grouped validation.
- Avoiding the use of future information during prediction.
- Working with anonymized data.

The target is based on observed performance signals and should not be treated as a confirmed business outcome.

## 8. Limitations

The project has some limitations:

1. The target is a proxy label and does not directly measure whether a content refresh will be successful.
2. Model performance may vary with different datasets and environments.
3. The model cannot fully understand content quality or search intent.
4. A high-priority score does not guarantee that updating a page will improve its performance.
5. Final content decisions require human review.

## 9. Future Improvements

Possible future improvements include:

- Testing on newer datasets.
- Improving feature selection.
- Exploring additional machine learning models.
- Improving ranking reliability.
- Adding more detailed explanations for recommendations.
- Monitoring model performance over time.

## 10. Reproducibility

The project was developed using Python and Google Colab.

To access the repository:

```bash
git clone https://github.com/piasa19/flyrank-ml-internship-starter.git
cd flyrank-ml-internship-starter
pip install -r requirements.txt
```

For the capstone experiment, open the relevant notebook from the `work/notebooks/` directory in Google Colab and execute the cells in order.

Use the anonymized dataset and the dependencies specified in the repository.

## 11. AI Transparency

AI assistants, including ChatGPT, were used as learning and development support for understanding machine learning concepts, structuring code, troubleshooting errors, and improving documentation.

The project workflow, notebook execution, validation checks, and interpretation of results were reviewed as part of my own work.

AI assistance was used as a support tool rather than a replacement for understanding and reviewing the project.

## 12. Conclusion

This project provided practical experience in data analysis, feature engineering, machine learning, model evaluation, and validation.

It demonstrates how machine learning can support content prioritization and help teams make more informed decisions.

The final output is intended to assist human decision-making rather than replace it.

---

**Project:** Content Refresh Prioritization Using Machine Learning  
**Author:** Piasa Das  
**Organization:** FlyRank AI
