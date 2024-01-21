# What even is dask?
- Certainly! Let's explore the differences between **Dask**, **Dask-distributed**, and **Dask-jobqueue**:
  
  1. **Dask**:
	- **Dask** is a flexible parallel computing library in Python.
	- It allows you to parallelize your code across multiple cores on a single machine or even scale out to a cluster of machines.
	- Dask provides high-level abstractions like **Dask Arrays**, **Dask DataFrames**, and **Dask Bags** that mimic NumPy, Pandas, and Python lists, respectively.
	- It's particularly useful for handling larger-than-memory datasets and performing distributed computations.
	- **Dask** itself doesn't directly interact with job queueing systems.
	  
	  2. **Dask-distributed**:
	- **Dask-distributed** is an extension of Dask that facilitates parallel execution across many computers.
	- It creates a **Dask Scheduler** that coordinates computation across a cluster of machines.
	- In **Dask-distributed**:
		- A **Worker** is a Python object and node in a Dask Cluster that serves two purposes:
		    1. Serve data (e.g., read data from disk or memory).
		    2. Perform computations (e.g., execute tasks).
		- The **Scheduler** manages the distribution of tasks to workers.
	- It's commonly used for distributed computing on clusters, cloud environments, or multi-node setups.
	  
	  3. **Dask-jobqueue**:
	- **Dask-jobqueue** is a Python package built to facilitate deploying Dask on High-Performance Computing (HPC) clusters.
	- It interfaces with various job queuing systems (e.g., PBS, SGE) to manage resources.
	- Key points about **Dask-jobqueue**:
		- It creates a Dask Scheduler within the Python process.
		- You define job parameters (cores, memory, walltime, etc.) for a single job or compute node.
		- The cluster generates traditional job scripts and submits them to the job queue.
		- Each job may include one or more Dask workers.
		- When the cluster object is closed, it signals workers to shut down.
	- **Dask-jobqueue** simplifies deploying Dask on HPC clusters while maintaining a Pythonic interface.
	  
	  In summary, **Dask** provides the core parallel computing functionality, **Dask-distributed** extends it for distributed execution, and **Dask-jobqueue** streamlines deployment on HPC clusters.
	  
	  Source: Conversation with Bing, 12/13/2023
	  (1) How this works — Dask-jobqueue 0.8.2+2.gef45c0e.dirty documentation. https://jobqueue.dask.org/en/latest/howitworks.html.
	  (2) python - Job, Worker, and Task in dask_jobqueue - Stack Overflow. https://stackoverflow.com/questions/72107679/job-worker-and-task-in-dask-jobqueue.
	  (3) Dask-jobqueue. https://blog.dask.org/2018/10/08/Dask-Jobqueue.
- # Dask tips and tricks
- Count the number of workers
	- `len(<client_name>.scheduler_info()['workers'])`
- Dask worker dying too fast
	- https://github.com/dask/dask/issues/3484
- # Questions
- Can dask adjust the number of workers it is running?
	- Web resources
		- https://dask.discourse.group/t/change-number-of-workers-during-runtime/1458