# AppMod Executive HTML Report Prompt Template (English)

## How to Use
Copy the entire prompt below into Copilot Chat or any large language model, then replace these placeholders:
- `{{report_json}}`
- `{{result_json}}`

---

You are an enterprise presentation designer and an application modernization architecture advisor.
Based on the input `report_json` and `result_json`, generate **a complete, premium HTML report with rich visuals that is suitable for executive presentation**.

### Input Data
- report_json: {{report_json}}
- result_json: {{result_json}}

### Mandatory Output Requirements
1. Output only one complete HTML document, starting with `<!doctype html>` and ending with `</html>`.
2. The output language must be English.
3. Do not output Markdown, explanations, or code fences.
4. The HTML must be directly savable as `report.html` and viewable in a browser.

### Presentation Positioning
1. Target audience: management and executive decision makers. The tone must be premium, concise, and conclusion-driven.
2. Ignore low-level technical details. Focus on value, risk, priority, and action plan.
3. The content must emphasize decision readiness so the next investment direction is immediately clear.

### Page Structure (Fixed Order)
1. Cover section: report title, subtitle, project name, date, and target platform
2. One-page executive summary with 3 to 5 key conclusions
3. Core KPI dashboard: total projects, issues, incidents, and total effort
4. Risk landscape: severity distribution and category distribution
5. Top risks and priorities: P0, P1, and P2
6. Strategic recommendations and business benefits: cost reduction, efficiency gains, and risk reduction
7. 30/60/90-day roadmap
8. List the existing application deployment resources, then list the post-migration Azure resources, then estimate the cost on Azure
9. Appendix: field mapping explanation

### Chart and Visual Requirements (Modern and Premium)
1. The page must follow the digital executive dashboard style of top-tier consulting firms such as McKinsey or Gartner:
	- A highly modern UI with strong technology and business value, preferably using glassmorphism, advanced gradients, and dynamic lighting effects.
	- KPI cards must deliver strong visual impact.
	- Use a premium color palette, for example deep blue, tech cyan, energetic orange, and alert red.
	- Use consistent rounded corners, shadows, whitespace, and polished layout.
2. **You must use a modern charting library such as ECharts via CDN**, with rich and interactive visualizations. Include at least:
	- **A modern radar chart** for dimensions such as cloud-native readiness, security, and scalability.
	- **A gauge chart** showing overall migration health or risk index.
	- **An animated donut chart** for severity distribution with highlight effects.
	- **A gradient bar chart** for issue category distribution.
	- **A line chart or area chart** showing estimated cost reduction or performance improvement after modernization.
3. External CDNs such as ECharts, Tailwind CSS, and Google Fonts are allowed and encouraged to maximize visual quality.

### Copywriting and Content Requirements (Emphasize Benefits)
1. **You must substantially expand the Business Value and ROI section**, using persuasive executive language.
2. Emphasize the specific benefits of modernization:
	- **Cost optimization and efficiency gains** such as lower TCO and reduced operations effort.
	- **Business agility** such as faster release cycles and elastic scaling.
	- **Security and compliance** such as enterprise-grade security baselines and zero-trust alignment.
3. Lead with conclusions, use short sentences, and avoid dense technical jargon. The tone should reflect strategy, operating perspective, and return on investment.
4. Keep each section to 3 to 6 key points, and highlight important numbers and keywords clearly.

### Data and Constraints
1. Use only information that can be identified from the input JSON.
2. Present results aggregated by `ruleId`, not incident-by-incident.
3. Do not invent project background, budget values, SLA targets, or go-live commitments.
4. If scan errors exist, summarize them briefly in a management-style risk notice.

### Styling and Technical Requirements
1. Use inline `<style>` and `<script>` so the report is fully deliverable as a single file.
2. Optimize for 1366+ wide-screen presentation and remain usable on standard laptop resolutions.
3. Tables must look business-ready, with clear headers, zebra striping, and highlighted key rows.
4. Support printing, and you may add `@media print` optimization.

### Field Mapping Notes (Must Appear at the Bottom)
- `summary.totalIssues` -> Total Issues
- `summary.totalIncidents` -> Total Incidents
- `summary.totalEffort` -> Total Effort
- `summary.charts.severity` -> Severity Distribution
- `summary.charts.category` -> Category Distribution

Now generate the final HTML document.