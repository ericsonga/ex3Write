..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. setup for automatic question numbering.

.. 	qnum::
	:start: 1
	:prefix: 4-2-
	
.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button
	
.. |pass| image:: Figures/pass.png
    :height: 20px
    :align: top
    :alt: pass
    
.. |start| image:: Figures/start.png
    :height: 24px
    :align: top
    :alt: start
    
.. |finish| image:: Figures/finishExam.png
    :height: 24px
    :align: top
    :alt: finishExam
    
.. |right| image:: Figures/rightArrow.png
    :height: 24px
    :align: top
    :alt: right arrow for next page
   
Example 2: Find the Maximum Value
------------------------------------
    
Another common thing to do is find the maximum value in a list.  To do this create a variable to keep track of the maximum value found so far and initialize it to the first item in the list to start.  Then loop through all the indices in the list.  Each time through the loop get the current value at the index and test if the current value is greater than the saved maximum value.  If it is, then set the maximum value to the current value.  Return the maximum value.

Examples
========

For example ``getMaximum([9, 3, 8])`` should return 9 and ``getMaximum([-2, -1, -3])`` should return -1.

Run Code
=========

Click the |runbutton| button to run the tests that check that this code is working correctly.  All tests should print |pass| since this is correct code.   Scroll down to try to solve the practice problem below.

.. activecode:: Get_Max
   :nocodelens:

   # define the function
   def getMaximum(numList):

       # init the maximum
       maximum = numList[0]

       # loop through indicies 
       for index in range(len(numList)):
       
           # get current at index
           current = numList[index]

           # if new max
           if current > maximum:

               # reset max
               maximum = current

       # return max
       return maximum
       
   ====
    
   # code to test the getMaximum function
   from unittest.gui import TestCaseGui
       
   class myTests(TestCaseGui):

       def testTarget(self):
           self.assertEqual(getMaximum([9, 3, 8]), 9, "Test of getMaximum([9, 3, 8])");
           self.assertEqual(getMaximum([-2, -1, -3]), -1, "Test of getMaximum([-2, -1, -3])");
           self.assertEqual(getMaximum([2, 3, 5, 15]), 15, "Test of getMaximum([2, 3, 5, 15])");
           self.assertEqual(getMaximum([32, 64, 28]), 64, "Test of getMaximum([32, 64, 28])");
           self.assertEqual(getMaximum([3]), 3, "Test of getMaximum([3])");
           
   myTests().main()
   
Practice 2: Find the Minimum Value
------------------------------------
   
The following code should find and return the minimum value in a list, but it contains errors.  To find the minimum value, create a variable to keep track of the minimum value found so far and initialize it to the first item in the list.  Then loop through all the indices in the list.   Each time through the loop get the current value. If the current value is less than the saved minimum value, then set the minimum value to the current value.  Return the minimum value.

.. note ::
   
    Remember that you should set the minimum value found so far to the first value in the list, rather than set it to 0. The list may not include a 0 so this wouldn't be the minimum value in the list.
    
Examples
=========

For example ``getMinimum([9, 3, 8])`` should return 3 and ``getMinimum([-2, -1, -3])`` should return -3.

Write Code Here
================

Finish writing the function below so that the code compiles and all the tests print |pass| when you click the |runbutton| button.  Any error messages and test results will be displayed below the code.

Click on the |start| button below when you are ready to try to order this code.  You will have up to 10 minutes to try to solve it.  Click the |runbutton| button to check your solution.  Click on the |finish| button when you have solved this problem or wish to move on without solving it.

.. timed:: get_min_write_timed
   :timelimit: 10
   :noresult:
   :nofeedback:
   :fullwidth:
   
   .. activecode:: Get_Min_Write
   
      # Finish the function getMinimum that takes a list of 
      # numbers and returns the minimum value in that list
      def getMinimum(numList):
  
      ====
       
      # code to test the getMinimum function
      from unittest.gui import TestCaseGui
       
      class myTests(TestCaseGui):

          def testTarget(self):
              self.assertEqual(getMinimum([9, 3, 8]), 3, "Test of getMinimum([9, 3, 8])");
              self.assertEqual(getMinimum([-2, -1, -3]), -3, "Test of getMinimum([-2, -1, -3])");
              self.assertEqual(getMinimum([2, 3, 5, 15]), 2, "Test of getMinimum([2, 3, 5, 15])");
              self.assertEqual(getMinimum([32, 64, 28]), 28, "Test of getMinimum([32, 64, 28])");
              self.assertEqual(getMinimum([3]), 3, "Test of getMinimum([3])");
           
      myTests().main()

When you are finished with this problem, or are ready to move on, click the |finish| button and then go to the next page by clicking the right arrow |right| near the bottom right of this page.    
