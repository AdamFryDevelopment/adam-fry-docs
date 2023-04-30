Batch Jobs
++++++++++
Batch jobs allow you to perform a recurring task.  When creating a new batch job, the main components that are needed are: 

- Service class - performs the batch process
- Controller class - the entry point to create an instance of the batch job
- Data contract class - decribes parameters that are passed to batch job

.. note::
   Dynamics AX 2012 has another framework called RunBaseBatch that is deprecated so this documentation will focus on the supported framework SysOperationFramework instead.

.. toctree::
   :maxdepth: 2
   :caption: Contents
   :hidden:

   simple_batch_job