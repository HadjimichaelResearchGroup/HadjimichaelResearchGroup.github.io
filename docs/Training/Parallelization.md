## Parallelization

### What Is Parallel Computing?
**Parallel computing** is a style of computation that takes advantage of multiple compute resources to concurrently execute a discrete number of tasks. Parallel computing exists in contrast to **serial computing**, where the same number of tasks would be solved sequentially using a single compute resource. 

[//]: # "Traditionally, software is written for serial computation. In a classical coding example, a single CPU (or **core**) would execute a single script line by line until it reaches the end of the program. There may be loops and conditional statements included in the script, but functionally its execution happens serially. This process is analogous to how electricity would flow through a circuit that operates in series: element-by-element, one before the next, until reaching the end of the circuit. A problem with this type of script execution comes from the inclusion of intra-script nested loops; each iteration of the loop happens one by one, even though the previous iteration of the loop might have no effect on the following iteration. Generally, this serialization/bottlenecking causes a massive slowdown in performance, especially if the dataset the script is processing is large. If it were possible to decentralize the nested loops and have each independent element run concurrently, we could expect a massive speedup in execution time."

[//]: # "This is the power of parallel computing. It utilizes the massive amount of compute resources granted by accessing additional cores to run independent loop iterations concurrently. The more cores you have access to, the greater performance you'll (generally) get. Accordingly, Penn State's ROAR Collab cluster is an ideal space for parallelization."

### How Do I Parallelize My Code?
The process needed to parallelize your code comes in two parts: (1) conceptually figuring out *if* your code can be parallelized at all (and then where and how much), and; (2) communicating to the cluster that you want your code to run in parallel. For the majority of the group's purposes, your code can be parallelized -- *and would benefit from parallelization* -- if you have a repeated process where each iteration is independent of any other. If you have script elements that do depend on previous iterations these could be rewritten for indepedence, but if that's not possible, you've found the extent of how parallel your code can execute. There are other reasons why parallelism might be beneficial for your scripting but they are outside the purview of this training.

Penn State's ROAR Collab provides several ways to tell the cluster you want to run a job in parallel.
[Clicking this link will take you to a presentation detailing how to parallelize your code](https://pennstateoffice365-my.sharepoint.com/:p:/r/personal/azh5924_psu_edu/Documents/Hadjimichael%20Group%20Materials/Training/Joining%20and%20Using%20the%20Cluster/ParallelizationTraining.pptx?d=w106ee2d33e3b43f6bbe8e7b56364f7b2&csf=1&web=1&e=b6Dnco). This presentation also has shell templates for scheduling jobs that utilize the `parallel` module. 

### I'd Still Like to Learn More About Parallelization
There are truly a gargantuan number of resources for you to learn more about parallel computing. We've compiled some additional resources below:
* [Topics in Parallel and Distributed Computing (via ICDS)](https://tcpp.cs.gsu.edu/curriculum/?q=cedr_book)
* [Parallel Computing (via Wikipedia)](https://en.wikipedia.org/wiki/Parallel_computing)
* [Data Parallelism (via Wikipedia)](https://en.wikipedia.org/wiki/Data_parallelism)
* [Introduction to Parallel Computing Tutorial (via Lawrence Livermore National Lab)](https://hpc.llnl.gov/documentation/tutorials/introduction-parallel-computing-tutorial)
* [Parallel Computing (via University of Sheffield)](https://docs.hpc.shef.ac.uk/en/latest/parallel/index.html#gsc.tab=0)
* [Introduction to Parallelism (via cwant.github.io)](https://cwant.github.io/hpc-beyond/21-introduction-to-parallelism/index.html)
