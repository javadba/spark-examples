# spark-examples

This example contains code for running dl4j on spark standalone as well as normal spark.

Dl4j interops with spark via dedicated classes and workers that take a spark context and a neural net configuration.

Underneath the covers we create the associated RDDs and other things that allow us to distributed neural net training on a cluster.

We scale out via hog wild and iterative reduce parameter averaging.

https://github.com/jpatanooga/KnittingBoar/wiki/Iterative-reduce




#Nd4j on spark

To run spark with different backends, just include the backend you want to use on the class path. When these jar files are included on the classpath, those will  included as part of the jar file for spark-submit.

To see more on this please read:

https://spark.apache.org/docs/latest/quick-start.html


If you run mvn clean package on spark for a spark job, the backends you include in the pom.xml will already be included.

You can create a jar file appropriate for spark-submit via the maven shade plugin (included in this pom). You can also run spark standalone. We have 1 example for each.



#Spark.ml
If you would like to use the newer spark.ml, please see:
https://github.com/deeplearning4j/dl4j-spark-ml-examples
