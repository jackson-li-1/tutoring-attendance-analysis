# Tutoring Center Utilisation & Attendance Analysis

## Question
When are tutoring sessions best and worst attended, and what drives demand at the center?

## Data
2,035 tutoring session records (Jan 26 - Apr 22, 2026) with modality, subject, date, time slot, student program affiliation, and attendance status (Attended, Cancelled, No Show). The data is private and not included in this repository, so the upload cell in the notebook will not run without the original file.

## Method
- Cleaned inconsistent text (extra spaces, capitalisation, typos in time slots) with pandas
- Defined attendance as status = "Attended" (cancellations and no-shows count as not attended)
- Compared attendance by time slot (slots with 100+ sessions), subject, program, and modality
- Tested the best vs. worst time slot with a chi-square test of independence
- Originally prototyped in Excel (pivot tables); rebuilt and extended in Python (pandas, matplotlib, scipy)

## Key findings
- Overall attendance was 79.3%.
- Attendance peaked at 82.9% for 12-1pm and was lowest at 66.4% for 7-8pm. The gap is statistically significant (chi-square p < 0.001).
- 4-5pm (73.7%) is also well below average, so the problem is not only the last slot of the day.
- Mathematics made up 43% of sessions.
- ASAP students made up 49% of sessions.
- 63% of sessions were in-person and 37% virtual.

## Recommendation
Shift tutor capacity from evening slots (especially 7-8pm) toward 12-3pm, and consider reminders or a virtual-only option for evening sessions.

## Limitations
This shows association, not cause. Evening students may differ in work schedules or commutes. The data covers one semester.

## Tools
Python, pandas, matplotlib, scipy, Google Colab
