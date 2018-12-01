/**********************************************************************
 *  Airport-readme template                                                   
 *  Airport Simulation (C++11 Concurrency)                       
 **********************************************************************/

Your name: Pitou Teng

Operating system you're using (Linux, OS X, or Windows): OS X, then switch to linux

If Windows, which solution?:

Text editor or IDE you're using: vim / visual studio code

Hours to complete assignment: 20 hours

/**********************************************************************
 *  Briefly discuss the assignment itself and what you accomplished.
 **********************************************************************/
using mutex, unique_lock, condition_variable to control data race 
and synchronize airplane threads


 /**********************************************************************
 *  Discuss one or more key algorithms, data structures, or 
 *  OO designs that were central to the assignment.
 **********************************************************************/
there is no data structures that is central to complete this assignment.
The only important thing we used is multi-threading's classes 
such as mutex, unique_lock, and condtion_variable


/**********************************************************************
 *  Briefly explain the workings of the features you implemented.
 *  Include code excerpts.
 **********************************************************************/
The following code excerpt if the runway mutex get unlocked 
in releaseRunways Function when the airplane is done using the runway.

    switch(runway){
    case AirportRunways::RUNWAY_4L :
        run4L.unlock();
        run15L.unlock();
        run15R.unlock();
    break;
    case AirportRunways::RUNWAY_4R :
        run4R.unlock();
        run15L.unlock();
        run15R.unlock();
        run9.unlock();
    break;
    case AirportRunways::RUNWAY_15R :
        run4L.unlock();
        run4R.unlock();
        run15R.unlock();
        run9.unlock();
    break;
    case AirportRunways::RUNWAY_15L :
        run4L.unlock();
        run4R.unlock();
        run15L.unlock();
    break;
    case AirportRunways::RUNWAY_9 :
        run4R.unlock();
        run15R.unlock();
        run9.unlock();                                                                                                                                                    
    break;
    case AirportRunways::RUNWAY_14 :
        run14.unlock();
    break;
    }


 /**********************************************************************
 *  Briefly explain what you learned in the assignment.
 **********************************************************************/
What I learned in this assignment is how to use c++ multi-threading classes
to control data races. It also gives me a better understand of how concurrency works


/**********************************************************************
 *  List whatever help (if any) you received from the instructor,
 *  classmates, or anyone else.
 **********************************************************************/
I worked with a classmate. His name is Scott.


/**********************************************************************
 *  Describe any serious problems you encountered.  
 *  If you didn't complete any part of any assignment, 
 *  the things that you didn't do, or didn't get working.                  
 **********************************************************************/
The big problem I encountered is that I didn't know how mutex, unique_lock
and condition_variable works together. The understanding of how they works
is central to completing this assignment


/**********************************************************************
 *  List any other comments here.                                     
 **********************************************************************/
