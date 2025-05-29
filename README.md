# mytestset

import pandas as pd
from IPython.display import display

# 데이터 
data = {
    "study_hours":     [2, 3, 4, 5, 6, 7, 8, 2, 3, 6],
    "sleep_hours":     [6, 7, 5, 6, 8, 5, 6, 4, 7, 6],
    "attendance_rate": [80, 85, 90, 95, 88, 92, 96, 70, 78, 94],
    "assignment_score":[60, 70, 75, 80, 85, 90, 95, 50, 65, 88],
    "part_time_hours": [10, 8, 5, 3, 4, 2, 0, 12, 9, 1],
    "exam_score":      [65, 70, 78, 85, 88, 92, 95, 55, 68, 90]
}

df = pd.DataFrame(data)


pearson_corr = df.corr(method="pearson").round(6)
spearman_corr = df.corr(method="spearman").round(6)
kendall_corr = df.corr(method="kendall").round(6)


display(pearson_corr)
display(spearman_corr)
display(kendall_corr)
