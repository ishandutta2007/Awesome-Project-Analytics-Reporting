# Awesome-Project-Analytics-Reporting

# Top Project Analytics & Reporting Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Sprint Metrics, Portfolio Dashboards & Self-Hosted Reporting Engines*  
**Last updated: November 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Project Analytics & Reporting**. These tools enable teams and PMOs to turn raw project data—issues, sprints, time logs, and budgets—into actionable insights, tracking velocity, spotting bottlenecks, and reporting progress to stakeholders without manual spreadsheet exports.

**Examples** include Jira Reporting, Screenful, Tableau, Power BI, Looker, eazyBI, Zoho Analytics, Domo, Datadog Project Analytics, and GoodData (the category leaders).

**Open-source emphasis**: Project Analytics & Reporting is a domain where open-source tooling is **surprisingly capable at the data layer but requires assembly for turnkey reporting**. **Apache Superset** and **Metabase** provide mature, self-hosted BI platforms that can connect to project databases (Redmine, OpenProject, Jira exports) for custom dashboards. For project-specific analytics, **OpenProject** is actively building native reporting—its roadmap includes sprint reports, burndown/burnup charts, velocity charts, cumulative flow diagrams, and epic progress views, addressing gaps teams migrating from Jira's plugin ecosystem have complained about . **Redmine Reporting** (likehopper) adds interactive dashboards with issue flow, time consumption, backlog tracking, and Chart.js visualizations directly within Redmine . The critical caveat: **commercial tools like Screenful and eazyBI are purpose-built for project data**—Screenful's Analytics 2 engine handles advanced metrics and AI-assisted chart creation , and eazyBI provides MDX-based OLAP analysis for Jira with 2026 additions like AI agent summaries and terminal-based CLI management . Open-source BI requires you to build the project-specific metrics yourself.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Jira Reporting](https://www.atlassian.com/software/jira/guides/reports-dashboards/overview)**  
  Native reporting and dashboards within Jira; built-in reports cover agile metrics (burndown, velocity, sprint), DevOps (deployment frequency), issue analysis, and forecasting . Dashboards aggregate gadgets across projects for real-time tracking. **Limitation**: advanced analytics and AI-powered space insights may require Premium or Enterprise tiers .

- **[Screenful](https://screenful.com/)**  
  Project analytics platform for Jira, Trello, ClickUp, and other task management tools. **Analytics 2 engine** (fully deployed Q1 2025) delivers faster chart loading and advanced analytics cases . Features: **15 chart types**, 100+ templates, **AI assistant** for natural-language chart creation ("Show me tasks completed this month grouped by label"), daily grouping, click-through drill-downs, and scheduled reports via email/Slack/PDF . **Note**: Dashboards product was sunset January 1, 2025 in favor of the new analytics engine .

- **[eazyBI](https://docs.eazybi.com/)**  
  OLAP-based reporting for Jira and Confluence with **MDX** for complex calculated measures. 2026 additions: **Rovo AI agent integration** for report summaries and insights, **eazyBI CLI** for terminal-based account/report management, AI agent skill for programmatic access, and refreshed dashboard design . **Best for teams wanting deep, multi-dimensional analysis** of Jira data—but it is a specialized add-on, not a standalone BI platform.

- **[Tableau](https://www.tableau.com/)**  
  Enterprise visual analytics; widely used for project and portfolio dashboards when connected to a data warehouse or Jira exports. Requires analyst resources for custom project metrics.

- **[Power BI](https://powerbi.microsoft.com/)**  
  Microsoft's BI platform; common for project reporting in Microsoft-centric organizations, with DAX for custom metrics and Power Query for data transformation.

- **[Looker](https://looker.com/)**  
  Google Cloud BI platform built on LookML for governed metric definitions; strongest when standardized on BigQuery for unified project and financial data.

- **[Zoho Analytics](https://www.zoho.com/analytics/)**  
  BI and analytics platform within the Zoho ecosystem; can connect to Zoho Projects and other Zoho apps for project reporting.

- **[Domo](https://www.domo.com/)**  
  Cloud BI platform with a broad connector library; positioned for operational and executive reporting across project and business data.

- **[Datadog Project Analytics](https://docs.datadoghq.com/)**  
  Analytics within Datadog for product and engineering data; while not a dedicated project management reporting tool, it can track custom events and metrics relevant to project health . **Best for engineering teams** already using Datadog for observability who want project metrics alongside infrastructure data.

- **[GoodData](https://www.gooddata.com/)**  
  Embedded analytics and BI platform; can be used to embed project dashboards into internal tools and customer-facing applications.

## Open-Source GitHub Projects

### Project Management Platforms with Native Reporting

- **[OpenProject](https://github.com/opf/openproject)**  
  Open-source project management (GPLv3 Community Edition) with **native reporting actively under development**. The roadmap (shared for community feedback) includes **sprint reports** (planned vs. completed vs. added mid-sprint), **burndown/burnup charts** with scope change visibility, **velocity charts**, **epic progress views**, **created vs. resolved charts** for backlog health, and **cumulative flow diagrams** for Kanban teams . **Current state**: concepts and early prototypes as of August 2026—not yet finished features . **Best for teams already on OpenProject** wanting integrated reporting—but expect to supplement with external BI until native reporting matures.

- **[Redmine Reporting (likehopper)](https://www.redmine.org/plugins/redmine_reporting)**  
  Open-source Redmine plugin (v1.2.1, compatible with Redmine 5.0–7.0) adding **interactive project dashboards** with Chart.js . Features: **issue flow tracking**, activity monitoring, **time consumption and backlog** charts, workload/team reporting (open issues and remaining effort by assignee), burnup charts with version changes and reopened issues, and **configurable annual time credits** . Charts link directly to Redmine's native issue/time-entry lists while respecting project permissions. **Best for Redmine users** wanting embedded dashboards without a separate BI tool—but it is plugin-specific and requires Redmine 5.0+.

### General-Purpose BI Platforms (Build Your Own Project Dashboards)

- **[Apache Superset](https://github.com/apache/superset)**  
  Leading open-source BI platform (Apache 2.0) with 40+ chart types, SQL Lab, RBAC, and row-level security. **Can connect to project databases** (Redmine's MySQL/PostgreSQL, OpenProject's PostgreSQL, Jira exports) for custom project dashboards. **Best for teams with SQL skills** wanting full control over metrics and visualization—but requires data modeling and dashboard building from scratch.

- **[Metabase](https://github.com/metabase/metabase)**  
  Open-source BI tool (AGPL) designed for non-technical users with a visual query builder; lighter than Superset and easier to deploy. **Can be connected to project databases** for self-service reporting. **Best for mixed teams** where project managers need to build their own reports—but project-specific metrics (sprint velocity, burndown) must be defined manually.

### Additional Strong Open-Source Options

- **RedmineUP Agile** — Commercial plugin (paid) for Redmine with agile charts and reporting; **not free** but often recommended for Redmine users wanting Jira-like agile reporting . **Verify licensing** before adoption.
- **oss-stats** — Open-source tool for tracking **open-source community health metrics** (PR response time, CI health, pipeline visibility) . **Niche**—for OSS maintainers rather than general project analytics, but demonstrates the pattern for automated project health reporting.

**Frameworks for building custom systems**: For **Redmine users**, Redmine Reporting provides embedded dashboards with issue flow and time tracking . For **OpenProject users**, native reporting is in active development—expect to use Superset/Metabase in the interim . For **general project data**, Superset or Metabase can be connected to project databases for custom dashboards. **No open-source project matches Screenful's AI-assisted chart creation or eazyBI's MDX-based OLAP depth** —those are commercial advantages for project-specific analytics.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Project analytics platforms handling project and performance data must comply with organizational governance policies; **self-hosted solutions place full responsibility for data pipeline reliability, metric accuracy, and access controls on the operator**.
- **Open-source project analytics is strongest at the BI layer but requires assembly for project-specific reporting**—Superset and Metabase provide mature visualization, and Redmine Reporting provides embedded dashboards . However, **no open-source project matches Screenful's AI-assisted chart creation or eazyBI's OLAP depth for Jira** . OpenProject's native reporting is in active development but not yet complete . Choose based on whether you need a general BI platform (Superset, Metabase) or project-embedded dashboards (Redmine Reporting, OpenProject's roadmap).
- Verify license terms for commercial use; Superset uses Apache 2.0, Metabase uses AGPL, and Redmine Reporting is a Redmine plugin (check repository for license).

---

**Made for project managers, PMO analysts, and teams building project reporting infrastructure.**  
Let's make project analytics more open, but with clear eyes about the project-specific metric engineering that commercial tools still handle out of the box.
