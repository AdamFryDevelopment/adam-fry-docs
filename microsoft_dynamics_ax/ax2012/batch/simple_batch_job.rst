Create a simple batch job
+++++++++++++++++++++++++
Create a basic batch job using SysOperation framework.  This batch job will make use of the existing base controller class SysOperationServiceController so we only need to create a service class to perform a function that can be run in batch.  This is as easy as creating a class and a menu item.  In this example, we'll create a batch job that *processes* CustTrans records.

Simple batch service class
==========================
Create a new class for the service.  The best practice is to suffix the class name with "Service".

.. code-block::

    class CustTransProcessService
    {
    }

Add a method to perform the batch process: 

.. code-block:: 

    public void processCustTrans()
    {
       CustTrans custTrans;

       ttsbegin;
       while select forupdate custTrans 
          where custTrans.IsProcessed == false
       {
          // do processing 

          custTrans.IsProcessed = true;
          custTrans.update();
       }
       ttscommit;
    }

Action Menu Item
=================
Now that we have a service class, we need an action menu item to that can point to it.  

.. csv-table:: ActionMenuItemProperties
   :header: Property, Description

   Name, Give it a name - I like to match the name of the service class
   Label, Give it a label that users can understand
   Oject type, Class
   Object, SysOperationServiceController
   Parameters, ServiceClass.MethodName i.e. CustTransProcessService.processCustTrans

Testing
=======
Compile the class and menu item and generate incremental CIL.  Then you can run the action menu item.  