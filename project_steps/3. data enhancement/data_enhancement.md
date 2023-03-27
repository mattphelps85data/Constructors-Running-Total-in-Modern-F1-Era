
# Step 3: Data Enhancement and Transformation

Now we need to add running total to our data set

### Insert Running Total Columns

Sample of organized data

Step1: Add running total and replace existing point columns

| Row Labels | Ferrari | Mercedes | McLaren |
| ---------- | ------- | -------- | ------- |
| 5/13/1950  | 0       | 0        | 0       |
| 5/21/1950  | 9       | 0        | 0       |
| 5/30/1950  | 9       | 0        | 0       |
| 6/4/1950   | 9       | 0        | 0       |
| 6/18/1950  | 11      | 0        | 0       |
| 7/2/1950   | 15      | 0        | 0       |
| 9/3/1950   | 21      | 0        | 0       |
| 5/27/1951  | 27      | 0        | 0       |
| 5/30/1951  | 27      | 0        | 0       |
| 6/17/1951  | 37      | 0        | 0       |

Step 2: Transpose dataset with dates as columns

| Row Labels | 5/13/1950 | 5/21/1950 | 5/30/1950 | 6/4/1950 | 6/18/1950 | 7/2/1950 |
| ---------- | --------- | --------- | --------- | -------- | --------- | -------- |
| Ferrari    | 0         | 9         | 9         | 9        | 11        | 15       |
| Mercedes   | 0         | 0         | 0         | 0        | 0         | 0        |
| McLaren    | 0         | 0         | 0         | 0        | 0         | 0        |

Step 3: Insert team logo image URL column as 2nd column 

| Row Labels | Image URL                                                                                                                                   | 5/13/1950 | 5/21/1950 | 5/30/1950 | 6/4/1950 | 6/18/1950 |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------- | --------- | --------- | -------- | --------- |
| Ferrari    | https://www.freeiconspng.com/uploads/ferrari-logo-icon-png-0.png                                                                            | 0         | 9         | 9         | 9        | 11        |
| Mercedes   | https://soymotor.com/sites/default/files/styles/thumbnail_150x150/public/imagenes/equipo/logo-mercedes-f1-2021.png?h=a7e6d17b&itok=9QOsw_W2 | 0         | 0         | 0         | 0        | 0         |
| Red Bull   | https://soymotor.com/sites/default/files/styles/thumbnail_150x150/public/imagenes/equipo/logos-redbull-f1-2021.png?h=a7e6d17b&itok=G31BknrU | 0         | 0         | 0         | 0        | 0         |
| McLaren    | https://ih1.redbubble.net/image.2391004768.1671/st,small,507x507-pad,600x600,f8f8f8.jpg                                                     | 0         | 0         | 0         | 0        | 0         |
| Williams   | https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSNOJ9sGzz7g70HsMiy9kKohZYcN4t680QHzxo1sB_wkzz1zQ-yzC8_iA_wqHSJDsR2&usqp=CAU           | 0         | 0         | 0         | 0        | 0         |
| Renault    | https://www.group1renault.co.za/blog/wp-content/uploads/new-renault-logo-blogimage.png                                                      | 0         | 0         | 0         | 0        | 0         |

Step 4: Upload to Flourish.com

Step 5: Add hex codes to bar color (if desired)

