LOAD DATASET schools AS csv FROM Chicago_Public_Schools_-_Progress_Report_Cards__2011-2012_.csv @ url 'https://raw.githubusercontent.com/IITDBGroup/cs520/master/vizier/Chicago_Public_Schools_-_Progress_Report_Cards__2011-2012_.csv'

select Teachers_Score, Community_Area_Name from schools

SELECT Community_Area_Name,AVG(Teachers_Score) as avg_teacher_score FROM score_and_community
GROUP BY Community_Area_Name

CREATE Line Chart with Points aggregation FOR "community_teacher_score"

CREATE LENS ON score_and_community IMPUTE MISSING VALUES ON COLUMN 0

def print_avg_teachers(ds):
    for row in ds.rows:
        print(row.get_value('avg_teacher_score'))
vizierdb.export_module(print_avg_teachers)

ds = vizierdb.get_dataset('community_teacher_score')
vizierdb.get_module("print_avg_teachers")
print_avg_teachers(ds)

df = vizierdb.get_data_frame('community_teacher_score')
print(df[df.avg_teacher_score<30.0])
