# Superuser Impact Report
![Current Version](https://img.shields.io/badge/version-31-blue)

Insights into work patterns of superuser and the resulting impact

[Download Latest (ZIP)](https://github.com/microsoft/superuserimpact/archive/refs/heads/main.zip)

**Additional Resources:**
[Viva Insights Python Library](https://microsoft.github.io/vivainsights-py/), [Viva Insights R Library](https://microsoft.github.io/vivainsights/)

⭐ **Star this repository** to receive notifications about new template versions
👀 **Watch** for updates and announcements

<details open>
  <summary>▶️ <b>Super User Impact Dashboard Preview</b></summary>

  <br>

  <img src="https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/report-preview.gif" alt="Super User Impact Dashboard Preview" width="100%" />

</details>

---

<details open>
<summary><strong>✨ What's New</strong></summary>

<br>

- NEW 'Super User Impact' dashboard that explores the impact of Copilot on work patterns (& sentiment if available) and estimated value
- Static thresholds for usage tiers (clearer benchmarking)
- One click zoom into superusers
- Cross-team comparisons

</details>

---

<details open>
<summary><strong>📊 Why Study Super Usage & Insights You Can Explore</strong></summary>

<br>

Super usage patterns show how experimentation turns into durable habits. Identifying early signals and contextual attributes helps you:
- Replicate adoption paths
- Prioritize enablement
- Benchmark across teams
- Inspire the organization

**Super Usage Profile**
What defines super usage, which Copilot scenarios super users rely on, and whether their behavior shows early signs of workflow change.

**Work Impact**
How users progress into super users, is this population growing over time?

**Work Patterns**
The distinctive work patterns of super users—including meeting habits, collaboration behaviors, and after‑hours signals.

**How They Get Work Done**
How super users leverage Copilot across surfaces and features to drive productivity in their daily workflows.

**Value**
How assisted value differs between super users and everyone else, and what this reveals about the incremental impact of deep Copilot engagement.

</details>

---

<details open>
<summary><strong>📦 Templates</strong></summary>

<br>

This repository includes two Power BI templates:

**Super User Impact Templates**
- **Template - Super User Impact - (CSV Input).pbit**: Measures Copilot's impact on work patterns and productivity using CSV data. Includes estimated value and sentiment analysis.
- **Template - Super User Impact - (Viva Insights Input).pbit**: Same analytics with direct Viva Insights connection for continuous impact tracking.

**Choosing Your Setup:**
Use **CSV templates** for ad-hoc analysis, simpler setup, or easier sharing. Use **Viva Insights templates** for automatic refresh, real-time data, and ongoing executive dashboards.

</details>

---

<h1 style="margin-top:1.5em; font-size:2.1em;">Instructions</h1>

> ⚠️ **Disclaimer**  
> This is an experimental template. On occasion, you may notice small deviations from metrics in the Copilot Dashboard. We will continue to iterate based on your feedback. Currently available in English only.

---

## Step 1. Build the Person Query (Required for All Setups)

1. Open: [https://analysis.insights.cloud.microsoft/](https://analysis.insights.cloud.microsoft/) and go to Create Analysis.
   
   ![Landing page showing Create Analysis](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/VivaLanding1.png)
3. Select **Person Query** → *Set up analysis*.
   
   ![Person query card highlighted](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/PersonQuery.png)
   
5. Configure:
   - **Time period**: Last 6 months (rolling)
   - **Group by**: Week
   - **Metrics**: See sub-step 4 for required attribute selection.
   - **Filter**: Is Active = True (if available) - You can validate the number of employees here. 
   - **Attributes**: Include Organization and Function Type (others optional) - this is the last box on this page. 
6. Select **ALL required metrics** (missing one will cause blank visuals).  
   ![Required metrics screenshot](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/groupings.png)
7. Save & Run query. Wait until **Status = Completed** (first runs can take several hours). Do not export mid-processing.

---

## Step 2. Choose Your Power BI Setup Path

<details>
<summary><strong>Import a CSV File</strong></summary>

- Export results as CSV → Save clearly (e.g., `SuperUsagePersonQuery_YYYY-MM-DD.csv`).
- Open `Template Super Usage Analysis (CSV).pbit` → point to CSV file path.
- Save working PBIX and publish to Power BI service for sharing (manual refresh required for updates).

</details>

<details>
<summary><strong>Setup Direct Query to Viva Insights</strong></summary>

- From Person Queries page, copy link (row/link icon).  
  ![Query row showing link icon](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/AnalysisResultsLink.png)
- Extract **partitionId** and **queryId** from URL. Confirm 36 characters each.  
  ![Partition and Query IDs highlighted](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/CopyIdentifiers.png)
- Open `Template Super Usage Analysis (Direct Query).pbit` → paste IDs when prompted.
- Sign in with your work account. Initial load may take 1–3 minutes.
- Save PBIX and publish to Power BI workspace. No scheduled refresh required (Direct Query auto-refreshes weekly).

</details>

---

## Next Steps

<details>
<summary><strong>Validation & Troubleshooting</strong></summary>

**Checklist for success:**
- No errors on load  
- Fields pane includes expected tables  
- Executive Summary visuals populate (not all blank)  

**Common Mistakes & Fixes**  
| Symptom | Cause | Fix |
|---------|-------|-----|
| Blank visuals | Missing required metric(s) | Re-export/re-run query with full set |
| Missing slicers/labels | Skipped Org/Function Type | Add both attributes and reprocess |
| Trend calcs broken | Grouped by Month | Use Week grouping |
| Partial weeks | Exported mid-processing | Wait until Status = Completed |
| Distorted adoption rates | Didn't filter active users | Add Is Active = True |
| Load error | CSV open in Excel (Option 1) | Close file and retry |
| Direct Query blank | Wrong GUIDs or status not complete | Re-check IDs and query status |

</details>

<details>
<summary><strong>Publish / Distribute</strong></summary>

- Save your PBIX file after setup.  
- If using Direct Query, publish to a Power BI workspace and configure credentials (OAuth2).  
- If using CSV Import, publish the PBIX file but note that refreshes are manual.  

</details>

<details>
<summary><strong>Interpretation & Storytelling</strong></summary>

Leverage the guides below to frame your narrative and drive action:

- [Copilot Assisted Hours PBI Formulas Guide (PDF)](https://github.com/microsoft/superuserimpact/raw/main/PDF%20Guides/Copilot%20Assisted%20Hours%20PBI%20Formulas.pdf)
- [Copilot Studio Agents Report - Interpretation Guide (PDF)](https://github.com/microsoft/superuserimpact/raw/main/PDF%20Guides/Copilot%20Studio%20agents%20report%20-%20Interpretation%20Guide.pdf)
- [Superuser Impact Storyboard v4 (PowerPoint)](https://github.com/microsoft/superuserimpact/raw/main/Superuser%20Impact%20-%20Storyboard%20v4.pptx)

Use the included guides to:
- Create an executive-ready presentation
- Define what constitutes super usage internally
- Highlight early activation behaviors
- Recommend enablement actions per org or cohort

</details>

<details>
<summary><strong>Monitor with Automatic Refresh</strong></summary>

- Configure Published Report Refresh settings
- Navigate to [Power BI Web](https://msit.powerbi.com/home?experience=power-bi) (you may need to login)
- Find the Report and Semantic Model you just published.
- Hover over the Semantic Model and click on the icon as seen below:
![Refresh1](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/Refresh1.png)
- On this page, from the list of options available, click on Refresh and then configure your report as seen below in the screenshot, or as you best fits your needs.
  
![refresh](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/refresh.png)

  
- For Direct Query: Reports update automatically with each weekly Viva Insights refresh, but you will still need to update the published report refresh settings as seen above. 
- For CSV Import: Re-run your query, export a new CSV, and repoint the PBIX to the updated file.  
- Verify weekly that a new week of data appears.  
- Track emerging super users and adoption trends regularly.  

</details>

---

<details>
<summary><strong>💬 Feedback</strong></summary>

<br>

We want to hear your feedback and suggestions. Please reach out to keithmcgrane@microsoft.com and jordanking@microsoft.com.

</details>

---

<table align="center" width="100%" style="margin-top:2.2em; margin-bottom:1.7em;">
  <tr>
    <!-- Copilot Impact Banner (Left)-->
    <td style="vertical-align:top; text-align:center; width:50%;">
      <div style="
        display:block;
        margin:0 auto;
        width:340px;
        max-width:95vw;
        background: linear-gradient(94deg, #f9f6ff 0%, #e6f0fd 100%);
        border: 2px solid #b38cff;
        border-radius: 15px;
        box-shadow: 0 2px 16px #9a7fff20;
        padding: 1.1em 1.1em 1.05em 1.1em;
        ">
        <span style="color:#2a237a; font-size:1.13em; font-weight:600;">
          ✨ This report <b>wouldn't have been possible without the magic of GitHub Copilot.</b><br/>
          <span style="font-weight:500;">
            As a tribute, we have built this GitHub Copilot analytics report.<br/>
            <a href="https://github.com/microsoft/GitHubCopilotImpact" style="color:#29009f; font-weight:600; text-decoration:underline;" target="_blank">@microsoft/GitHubCopilotImpact</a> &mdash; try it out and give us feedback!
          </span>
        </span>
      </div>
    </td>
    <!-- AI-in-One Banner (Right)-->
    <td style="vertical-align:top; text-align:center; width:50%;">
      <div style="
        display:block;
        margin:0 auto;
        width:340px;
        max-width:95vw;
        background: linear-gradient(93deg, #eefcf5 0%, #e1edff 100%);
        border: 2px solid #17bcb8;
        border-radius: 15px;
        box-shadow: 0 2px 16px #24d6cd14;
        padding: 1.1em 1.1em 1.05em 1.1em;
        ">
        <span style="color:#086b65; font-size:1.13em; font-weight:600;">
          🤔 Curious how <b>free chat, M365 Copilot, and agent usage all connect?</b><br>
          <span style="font-weight:500;">
            Check out the companion report at<br>
            <a href="https://github.com/microsoft/AI-in-One-Dashboard" style="color:#005782; font-weight:600; text-decoration:underline;" target="_blank">@microsoft/AI-in-One-Dashboard</a>
          </span>
        </span>
      </div>
    </td>
  </tr>
</table>

