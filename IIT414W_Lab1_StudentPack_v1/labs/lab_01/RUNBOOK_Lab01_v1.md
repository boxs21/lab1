# Lab 1 · Runbook

1. Extract the complete package into your course repository; preserve labs/lab_01 and data/samples/lab01_v1.
2. Use your Week 2 Python environment. If needed: `python -m pip install -r requirements_lab01_v1.txt` from the package root.
3. Open labs/lab_01/Lab01_EDA_Baselines_Student_v1.ipynb with that environment's Python kernel. Default MODE is snapshot; no network is used by the notebook.
4. Work through train, then calibration. Complete the written evidence and freeze record before enabling RUN_TEST.
5. Restart and Run All after completing the notebook. Save its outputs. Confirm that you can reproduce the frozen evaluation without modifying decisions.
6. Record your actual Python/package versions, operating system, any changes to this procedure, the submitted commit and the date/result of your check below. Keep the source CSVs unchanged.

Actual environment and execution evidence:
- Kernel used for the saved notebook outputs: Python 3.14.3, pandas 2.3.1 (printed by the first notebook cell). numpy: [version]. matplotlib: [version].
- Machines: Andy Villarroel (macOS) and Agustín Reyes (Windows).
- Data mode: `snapshot` (local CSVs in data/samples/lab01_v1, no network, no API credentials). Source CSVs and lab01_manifest_v1.json unchanged.
- Changes to this procedure: none. One analysis correction (keeping the 3 rows with missing qualifying instead of dropping them) is documented in notebook section 5.
- Freeze commit (before RUN_TEST=True): [hash].
- Final Restart & Run All: [date] · result: [ran without errors / notes] · submitted commit: [hash].

Submission uses GitHub + Canvas as stated in the brief. Include support code and the six CSVs plus lab01_manifest_v1.json. No API credentials are needed. If your environment is blocked, record the exact error and contact the teaching team; do not label synthetic practice as real data.
