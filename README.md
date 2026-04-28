# Performance Testing - JMeter

1. /all-student
![tree](images/all-student-tree.png)
![table](images/all-student-table.png)
![summary](images/all-student-summary.png)
![graph](images/all-student-graph.png)

2. /all-student-name
![tree](images/student-name-tree.png)
![table](images/student-name-table.png)
![summary](images/student-name-summary.png)
![graph](images/student-name-graph.png)

3. /highest-gpa
![tree](images/highest-gpa-tree.png)
![table](images/highest-gpa-table.png)
![summary](images/highest-gpa-summary.png)
![graph](images/highest-gpa-graph.png)

Analysis
- /all-student is the slowest because it returns all data
- /all-student-name is faster because it returns fewer fields
- /highest-gpa is the fastest since it only returns one result

# command Line Results
/all-student
![all-student-cli](images/all-student-result.png)
![all-student-log](images/all-student-log.png)

/highest-gpa
![highest-gpa-cli](images/highest-gpa-result.png)
![highest-gpa-log](images/highest-gpa-log.png)

/all-student-name
![student-name-cli](images/student-name-result.png)
![student-name-log](images/student-name-log.png)