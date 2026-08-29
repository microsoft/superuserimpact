> [!IMPORTANT]
> **v13 is here** — this release adds compatibility with Viva Insights' newly consolidated Copilot Chat metrics (the old metrics are automatically rebuilt from the new merged ones, so every visual keeps working), and fixes a false "some Copilot Chat metrics are missing" warning plus a Power BI refresh error caused by a missing DisplayName column.
>
> **Download v13:** [CSV template](https://github.com/microsoft/superuserimpact/raw/main/Template%20-%20Super%20User%20Impact%20CSV%20-v13.pbit) &nbsp;&middot;&nbsp; [Direct Query template](https://github.com/microsoft/superuserimpact/raw/main/Template%20-%20Super%20User%20Impact%20Direct%20Query%20-v13.pbit)
>
> **Then update your Viva Insights query:** edit the query, open the **Microsoft 365 Copilot** metric selection, and re-check **Select all** so the newly consolidated Copilot Chat metrics are included in your export.

<div align="center">

<br>

# 🧠 Super User Impact

### Measure the real work-pattern impact of your Copilot super users.

<br>

[![Built by Microsoft](https://img.shields.io/badge/Built%20by-Microsoft-0078d4?style=for-the-badge&logo=microsoft&logoColor=white)](https://microsoft.github.io/Analytics-Hub/team/)
[![Analytics Hub](https://img.shields.io/badge/Analytics%20Hub-11%20Repositories-8661c5?style=for-the-badge&logo=github&logoColor=white)](https://microsoft.github.io/Analytics-Hub/)

<br>

**Found this useful? ⭐ Star this repo to help others discover it!**

<br>

**[What's New ↓](#whats-new)** &nbsp;·&nbsp; **[Preview ↓](#dashboard-preview)** &nbsp;·&nbsp; **[Watch First ↓](#-watch-first)** &nbsp;·&nbsp; **[Instructions ↓](#instructions)** &nbsp;·&nbsp; **[Next Steps ↓](#next-steps)** &nbsp;·&nbsp; **[Email your Admin ↓](#email-your-admin)**

<br>

</div>

---

<a id="whats-new"></a>

<details open>
<summary><strong>✨ What's New</strong></summary>

<br>

- NEW 'Super User Impact' dashboard that explores the impact of Copilot on work patterns (& sentiment if available) and estimated value
- Static thresholds for usage tiers (clearer benchmarking)
- One click zoom into superusers
- Cross-team comparisons

</details>

---

<a id="dashboard-preview"></a>

<details open>
  <summary>▶️ <b>Super User Impact Dashboard Preview</b></summary>

  <br>

  <img src="https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/report-preview.gif" alt="Super User Impact Dashboard Preview" width="100%" />

</details>


<a id="-watch-first"></a>

## 🎬 Watch First

Plays here in the page — no download.

**A guided tour of the report** — measure the real work-pattern impact of your Copilot super users. *(1m 41s)*

https://github.com/user-attachments/assets/b8935dae-6936-42d2-9dec-5befd4a97d42


---

<details open>
<summary><strong>📊 Why Study Super Usage & Insights You Can Explore</strong></summary>

<br>

Super usage patterns show how experimentation turns into durable habits. Identifying early signals and contextual attributes helps you:
- Replicate adoption paths
- Prioritize enablement
- Benchmark across teams
- Inspire the organization

**Super usage profile:**
What does super usage look like? What do super users use Copilot for? Are you seeing signs of workflow changes?

**Journey:**
How did some users turn into super users? What did super users do differently in the early days of license activation? How fast are you producing super users? Is super usage durable?

**Work patterns:**
What work patterns are associated with super users? Are you seeing any early impact?

**Change management:**
Where are the super users concentrated? Where might you focus enablement efforts?

</details>

---

<a id="instructions"></a>

<details open>
<summary><strong style="font-size:1.5em;">📋 Instructions</strong></summary>

<br>

![Viva Insights Query Setup Guide](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/viva_insights_setup.gif)

<details>
<summary><strong>Written Setup Guide</strong></summary>

<br>

### Step 1. Build the Person Query (Required for All Setups)

Open the [Viva Insights Analyst Workbench](https://analysis.insights.cloud.microsoft/) and follow this 5-step process to create your Person Query:

<details>
<summary><strong>Detailed step-by-step guide with screenshots</strong></summary>

<br>

![Detailed Query Setup Guide](https://raw.githubusercontent.com/microsoft/superuserimpact/main/images/viva_insights_query_setup_static.png)

### Quick Reference:

1. **Navigate to Analysis Results**
   - Go to [https://analysis.insights.cloud.microsoft/](https://analysis.insights.cloud.microsoft/)
   - Click on "Analysis results" in the left sidebar

2. **Create New Person Query**
   - Click "Create analysis"
   - Select "Person query" card
   - Click "Set up analysis"

3. **Configure Query Settings**
   - **Time period**: Last 6 months (rolling)
   - **Group by**: Week
   - **Filter**: Is Active = True
   - **Attributes**: Organization, FunctionType, TimeZone (minimum required)

4. **Select Required Metrics**
   - **Microsoft 365 Copilot**: Select "All metrics"
   - **Collaboration network**: Select "All metrics"
   - **Working hours collaboration**: Select "All metrics"
   - **Focus metrics**: Select "All metrics"
   - Missing even ONE metric will cause blank visuals in Power BI!

5. **Run and Wait for Completion**
   - Save & Run your query
   - Wait until **Status = Completed** (can take several hours for first run)
   - Do NOT export mid-processing
   - Once complete, copy your **Partition ID** and **Query ID** for Power BI

</details>

---

<a id="next-steps"></a>
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

- Super Usage Interpretation Guide (PDF): [Interpretation Guide Super Usage Adoption](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Interpretation%20Guide%20Super%20Usage%20Adoption.pdf)
- Storyboard presentation template: [Storyboard PPTX - Super User Adoption](https://github.com/microsoft/DecodingSuperUsage/blob/DecodingSuperUsage/Storyboard%20PPTX%20-%20Super%20User%20Adoption.pptx)

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

</details>

</details>

---

<details>
<summary><strong>🤓 Nerd Corner</strong></summary>

<br>

If you're into automation and allergic to manual decks — try this:

👉 https://github.com/shailendrahegde/pbi-to-exec-deck

It turns raw outputs into **exec-ready PPTs** with insights pre-baked.
All you do: verify, tweak, ship.

</details>

---

---

<a id="email-your-admin"></a>

> 📧 **Before you begin, your Viva Insights admin needs to set up a Person Query.**
> This pre-written email covers all required metric groups, query settings, attributes, admin roles, and connection options — everything your admin needs in one click.
>
> **[📨 Email Prerequisites to Your IT Admin](mailto:?subject=Action%20Required%3A%20Viva%20Insights%20Query%20Setup%20Needed%20for%20Super%20User%20Impact%20Report%20%28Power%20BI%29&body=To%3A%20IT%20Admin%20%2F%20Global%20Admin%20%2F%20Viva%20Insights%20Administrator%0ARe%3A%20Super%20User%20Impact%20%E2%80%93%20Power%20BI%20Report%20Setup%0A%0A%0AWHAT%20THIS%20REPORT%20DOES%0A%0AThe%20Super%20User%20Impact%20Report%20is%20a%20Power%20BI%20report%20powered%20by%20Viva%20Insights%20data.%20Where%20the%20Super%20User%20Adoption%20report%20tracks%20who%20super%20users%20are%2C%20this%20report%20measures%20what%20changed%20in%20their%20work%20patterns%20as%20a%20result%20of%20Copilot%20adoption%20%E2%80%94%20including%20collaboration%20hours%2C%20meeting%20load%2C%20focus%20time%2C%20and%20estimated%20time%20saved.%20Includes%20cross-team%20benchmarking%20and%20optional%20sentiment%20signal%20analysis.%20Used%20to%20demonstrate%20ROI%20and%20guide%20change%20management.%0A%0A%0ADATA%20SOURCE%20REQUIRED%0A%0AViva%20Insights%20%E2%80%93%20Person%20Query%0AExport%3A%20analysis.insights.cloud.microsoft%20-%3E%20Create%20analysis%20-%3E%20Person%20query%0AFormat%3A%20CSV%20or%20Direct%20Query%20%28via%20Partition%20ID%20%2B%20Query%20ID%29%0A%0A%0AREQUIRED%20FIELDS%20%E2%80%94%20DO%20NOT%20REMOVE%0A%0AIMPORTANT%3A%20This%20report%20uses%20the%20same%20Viva%20Insights%20Person%20Query%20as%20the%20Super%20User%20Adoption%20report.%20All%20metric%20groups%20must%20be%20selected%20in%20full.%20Partial%20exports%20or%20manually%20edited%20CSVs%20with%20removed%20columns%20will%20cause%20blank%20visuals%20and%20broken%20calculations.%0A%0APerson%20Query%20%E2%80%94%20Required%20Metric%20Groups%20%28select%20%22All%20metrics%22%20for%20each%29%3A%0AMicrosoft%20365%20Copilot%20%28all%20metrics%29%2C%20Collaboration%20network%20%28all%20metrics%29%2C%20Working%20hours%20collaboration%20%28all%20metrics%29%2C%20Focus%20metrics%20%28all%20metrics%29.%0A%0ASpecific%20fields%20the%20report%20depends%20on%3A%0ACopilot_Active_Use_Days_per_week%2C%20Copilot_Total_Actions%2C%20Copilot_Total_Chats%2C%20Collaboration_hours%2C%20Meeting_hours%2C%20After_hours_collaboration_hours%2C%20Email_hours%2C%20Meeting_hours_with_manager_1_on_1%2C%20Focus_hours%2C%20Uninterrupted_focus_hours%2C%20Internal_network_size%2C%20Strong_ties%2C%20Diverse_ties.%0A%0APerson%20Query%20%E2%80%94%20Required%20Attributes%20%28Dimensions%29%3A%0APersonId%2C%20Organization%2C%20FunctionType%2C%20TimeZone%2C%20IsActive.%0A%0AQuery%20Configuration%20%E2%80%94%20Required%20Settings%3A%0A-%20Time%20period%3A%20Last%206%20months%20%28rolling%29%0A-%20Group%20by%3A%20Week%20%28not%20Month%29%0A-%20Filter%3A%20Is%20Active%20%3D%20True%0A%0A%0AINSIGHTS%20YOU%20WILL%20GAIN%0A%0A-%20Work%20pattern%20delta%20analysis%3A%20how%20collaboration%20hours%2C%20meeting%20time%2C%20email%20time%2C%20and%20focus%20time%20differ%20between%20super%20users%20and%20their%20peers%0A-%20After-hours%20work%20impact%3A%20whether%20Copilot%20adoption%20correlates%20with%20better%20or%20worse%20work-life%20balance%20signals%0A-%20Time%20saved%20estimation%3A%20calculated%20value%20model%20based%20on%20total%20Copilot%20actions%0A-%20Network%20changes%3A%20whether%20super%20users%20have%20broader%20or%20deeper%20internal%20collaboration%20networks%0A-%20Cross-team%20benchmarking%3A%20compare%20impact%20signals%20across%20organizations%2C%20function%20types%2C%20and%20usage%20tiers%0A-%20Manager%201%3A1%20time%3A%20changes%20in%20coaching%20and%20alignment%20meeting%20patterns%0A%0A%0AROLES%20%26%20PERMISSIONS%20REQUIRED%0A%0ACreate%20and%20run%20Person%20Query%20in%20Viva%20Insights%3A%20Insights%20Analyst%20%28assigned%20in%20Viva%20Insights%20Admin%29%0AAccess%20Viva%20Insights%20Analyst%20Workbench%3A%20Insights%20Analyst%20or%20Insights%20Administrator%0AExport%20query%20results%20as%20CSV%3A%20Insights%20Analyst%0A%0A%0ASOFTWARE%20REQUIREMENTS%0A%0A-%20Power%20BI%20Desktop%20%E2%80%94%20required%20to%20open%20the%20.pbit%20template%20file%0A-%20Access%20to%3A%20analysis.insights.cloud.microsoft%20%28Viva%20Insights%20Analyst%20Workbench%29%0A-%20Microsoft%20365%20Viva%20Insights%20license%20%E2%80%94%20required%20for%20the%20organization%20to%20generate%20Person%20Query%20data%0A%0A%0ANote%3A%0AThe%20Super%20User%20Impact%20report%20uses%20the%20same%20Person%20Query%20as%20the%20Super%20User%20Adoption%20report.%20If%20both%20reports%20are%20being%20deployed%20simultaneously%2C%20a%20single%20query%20export%20can%20feed%20both%20templates%20%E2%80%94%20no%20need%20to%20run%20separate%20queries.)**

---

<details>
<summary><strong>💬 Feedback</strong></summary>

<br>

We want to hear your feedback and suggestions. Please reach out to keithmcgrane@microsoft.com and jordanking@microsoft.com.

</details>

---

<details>
<summary><strong>🔔 Stay Updated</strong></summary>

<br>

- ⭐ **Star this repository** to receive notifications about new template versions
- 👀 **Watch** for updates and announcements
- 🔄 Check back regularly for new features and improvements

</details>

---
