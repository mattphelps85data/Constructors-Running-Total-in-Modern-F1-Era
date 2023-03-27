
# Step 2: Data Organization

Now that we have a joined table, we need to prepare the dataset for Flourish data format.

### Excel Organization

Sample of initial joined data
 | date      | points | team_name   |
| --------- | ------ | ----------- |
| 5/13/1950 | 0      | Talbot-Lago |
| 5/13/1950 | 0      | Alfa Romeo  |
| 5/13/1950 | 9      | Alfa Romeo  |
| 5/13/1950 | 0      | Alta        |
| 5/13/1950 | 0      | Maserati    |
| 5/13/1950 | 0      | Maserati    |
| 5/13/1950 | 0      | ERA         |
| 5/13/1950 | 0      | Maserati    |

Step 1: Pivot this joined table

| Row Labels | March | Adams | AFM | AGS | Alfa Romeo | AlphaTauri |
| ---------- | ----- | ----- | --- | --- | ---------- | ---------- |
| 5/13/1950  |       |       |     |     | 19         |            |
| 5/21/1950  |       |       |     |     | 9          |            |
| 5/30/1950  |       | 0     |     |     |            |            |
| 6/4/1950   |       |       |     |     | 15         |            |
| 6/18/1950  |       |       |     |     | 18         |            |
| 7/2/1950   |       |       |     |     | 15         |            |
| 9/3/1950   |       |       |     |     | 13         |            |
| 5/27/1951  |       |       |     |     | 18         |            |
| 5/30/1951  |       |       |     |     |            |            |
| 6/17/1951  |       |       |     |     | 9          |

Step 2: Fill blank cells with 0

| Row Labels | March | Adams | AFM | AGS | Alfa Romeo |
| ---------- | ----- | ----- | --- | --- | ---------- |
| 5/13/1950  | 0     | 0     | 0   | 0   | 19         |
| 5/21/1950  | 0     | 0     | 0   | 0   | 9          |
| 5/30/1950  | 0     | 0     | 0   | 0   | 0          |
| 6/4/1950   | 0     | 0     | 0   | 0   | 15         |
| 6/18/1950  | 0     | 0     | 0   | 0   | 18         |
| 7/2/1950   | 0     | 0     | 0   | 0   | 15         |
| 9/3/1950   | 0     | 0     | 0   | 0   | 13         |
| 5/27/1951  | 0     | 0     | 0   | 0   | 18         |

Step 3: Save file and prepare for data transformation