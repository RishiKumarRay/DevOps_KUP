####                                       Day -6  Question/ Answer (jenkins)

##### Q1-  How to install plugin without using Jenkins GUI?

Ans- We can use the jenkins cli and with the below command we can install plugin

-java -jar jenkins-cli.jar -s http://myip:8080/ -webSocket install-plugin SOURCE ... [-deploy] [-name VAL] [-restart]

------



##### Q2- What is multi configuration project?

Ans- A multi configuration project is actually a project which focuses on testing in various environment.This helps in creating one job with many configuration. Thus each configuration runs as a separate job.This helps in simplifying our scheduled tests.

------



##### Q3 -What is new view?

Ans- A new view helps in organising our view as per our need.Like we have many jobs alligned and then we need only few jobs to be viewed on priority then we can use this view.

------



4. ##### What are executors in Jenkins?

ans - Executors are the primary building block of Jenkins whose main purpose is to execute a job. The number of executors denote the maximum number of concurrent build the project can have.

------

**5- How to access workspace from CLI?**

Ans - we can look in this directory /var/docker/jenkins_home/workspace

------

**6- . What are labels in Jenkins Master Slave?** 

Ans - Labels are used to group slave nodes or agents. So when executing a pipeline if a node in this label is running a job, it is executed by another node in the label.

------



7. **How to run jobs in parallel in Jenkins?**

Ans - n the pipeline use   `build 'Job-Name' `



