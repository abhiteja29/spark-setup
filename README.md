# spark-setup

### Processing data using spark and finding the mostly used top 10 words


## Step 1:
### Command used to create an RDD using either a local text file or a remote file link
### scala> val romeoRDD = sc.textFile("D:/sample.txt");

## Step 2:
### Command used to map the words
### scala> val wordCounts = textFile.flatMap(line => line.split(" ")).map(word => (word, 1)).reduceByKey((a, b) => a + b);

## Step 3:
### Command used to display the value
### scala> wordCounts.collect();

## Step 4:
### Command used to sort and display the result in descending order
### scala> var sortedData = wordCounts.sortBy(_._2,false).take(10);

## Step 5:
### Command used to display the first 10 values
### scala> val res10 = sortedResult.take(10);

# References
1. https://github.com/denisecase/setup-spark
2. https://alvinalexander.com/scala/how-to-sort-map-in-scala-key-value-sortby-sortwith/
3. https://spark.apache.org/docs/2.1.0/quick-start.html
