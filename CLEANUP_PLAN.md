# File Cleanup Plan for SkyGeni Challenge Submission

## ✅ Files to KEEP

### Essential Files:
1. **README.md** - Main submission document (already cleaned)
2. **part2_win_rate_decline_analysis_last2_Q.ipynb** - Part 2: EDA & Insights
3. **part3_decision_engine.ipynb** - Part 3: Decision Engine
4. **part5_reflection.md** - Part 5: Reflection
5. **skygeni_sales_data.csv** - The dataset

### Optional Reference:
6. **challenge_description.md** - Original challenge prompt (for context)

---

## ❌ Files to DELETE (Redundant/Outdated)

1. **eda.ipynb** - Old EDA version, superseded
2. **executed_eda.ipynb** - Large executed version (397KB), not needed
3. **part2_eda_insights_both_data.ipynb** - Redundant, superseded by win_rate_decline
4. **part2_insights_only_total.ipynb** - Large (502KB), redundant analysis
5. **business_insights_summary.md** - Insights now in README
6. **part3_decision_engine_answer.md** - Text version, analysis in notebook
7. **insights_summary.png** - Old visualization
8. **SkyGeni – Sales Intelligence Challenge.docx** - Original Word doc, not needed

---

## 📝 Recommended Action:

```bash
# Delete redundant files
rm eda.ipynb
rm executed_eda.ipynb
rm part2_eda_insights_both_data.ipynb
rm part2_insights_only_total.ipynb
rm business_insights_summary.md
rm part3_decision_engine_answer.md
rm insights_summary.png
rm "SkyGeni – Sales Intelligence Challenge.docx"
```

## Final Structure:

```
skygeni/
├── README.md                                    ← Main submission
├── part2_win_rate_decline_analysis_last2_Q.ipynb   ← Part 2
├── part3_decision_engine.ipynb                  ← Part 3
├── part5_reflection.md                          ← Part 5
├── skygeni_sales_data.csv                       ← Data
└── challenge_description.md                     ← Reference (optional)
```

This creates a clean, professional submission package that's easy for recruiters to navigate.
