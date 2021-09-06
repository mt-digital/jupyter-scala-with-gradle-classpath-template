# Scala in Jupyter with gradle classpath template
A template for using Scala in Jupyter with the Almond kernel that includes how to set a Gradle project's classpath

## The problem: accessing dependencies and local package code in Jupyter using the Almond kernel

I wanted to use the Jupyter notebook to make notes about a Scala & Java codebase I recently started working with as part of my work with the Lawrence Berkeley National Lab Sustatinable Transportation Institute's BEAM transportation modeling framework. It was not clear from available documentation how to tell the Almond/Scala interpreter what the Scala compiler classpath should be. The classpath tells the interpreter and compiler where to look for dependencies. For instance, BEAM uses the Akka library to represent transportation system entities as Actors ([Akka docs](https://doc.akka.io/docs/akka/current/index.html); [original CS paper on Actors by Hewitt, Bishop, and Steiger (1973)](https://eighty-twenty.org/files/Hewitt,%20Bishop,%20Steiger%20-%201973%20-%20A%20universal%20modular%20ACTOR%20formalism%20for%20artificial%20intelligence.pdf)). It would be nice to experiment with Actors and the BEAM entities that extend the Actor class.

This repository provides a minimal example of a Jupyter notebook that sets the classpath and imports from user-defined packages built to a gradle-defined classpath. 

