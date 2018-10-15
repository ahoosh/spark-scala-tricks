# spark-scala-tricks
Random Interesting notes on Spark using Scala

 ```
 val changeColumns = Map("col1_old" -> "col1_new",
                          "col2_old" -> "col2_new")
  df = df.select(df.columns.map(c => col(c).as(changeColumns.getOrElse(c, c))): _*)
  ```
