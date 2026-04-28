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

Performance Comparison
After optimization, the JMeter results show better performance compared to the initial run. 
The response time is lower and throughput is more stable, which means the optimization reduced unnecessary database calls and improved efficiency.

Reflection
1. JMeter focuses on testing performance from outside (like real users hitting endpoints), while IntelliJ Profiler looks inside the code to see which methods are slow or consuming resources.
2. Profiling helps me clearly see which method is taking the most time (like getAllStudentsWithCourses), so I know exactly what to optimize instead of guessing.
3. Yes, it’s effective because it directly shows CPU usage and execution time per method, making bottlenecks obvious.
4. The main challenge was inconsistent results and setup issues (like server not running or JMeter errors). I handled it by rerunning tests and making sure the app is stable before testing.
5. The biggest benefit is visibility, I can see exactly where time is spent, not just that something is slow.
6. I compare both: JMeter shows overall performance, profiler shows internal cause. If they don’t match, I recheck test conditions and run multiple times.
7. I optimized by reducing repeated database calls and using better queries. To make sure nothing breaks, I kept the logic the same and only changed how data is fetched.