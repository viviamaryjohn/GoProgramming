## Object Oriented Programming

Go language is object-oriented, more like weakly object oriented. It implements objects but maybe they have fewer features than you would see in another object-oriented language like Java, C++ or Python.

Let's look at a summary of object orientation.
1. Organize your code by *encapsulation*
2. Group together data and functions that are related
3. User-defined type which is specific to an application
   - ints have data (number) and functions (+, -, *, /)

### Object Example
Let's say you are implementing an application performing geometry in 3D. Many functions will be operating on *points*.
1. Each point has *data*
   - x, y and z coordinates
2. Points also have *functions*
   - DistToOrigin(), Quadrant()
3. You can define a Point *class* that defines data and functions. Where data x, y and z can be of floating point type and you can defined what the functions are supposed to do.
4. Point *objects* are instances of class.

## Objects in Go
1. Go does not use the term *class*
2. Go uses *struct* with associated methods
3. Simplified implementation of classes
   - No inheritance
   - No constructors
   - No generics
4. Easier to code (if you like the object oriented features, then this is a disadvantage)

## Concurrency

**Performance Limits**
*Moore's Law* - the number of transistors on a chip doubles every 18 months.
> It used to help in performance. This used to be the case before, not recently. Because of doubling of transistors, the transistors got smaller and would be closer to each other and the clock rate would increase. Power/temperature constraints limit clock frequencies now.
So, how do you get performance improvement even though you can't just crank up the clock?
One way to do this is to use *Parallelism*

### Parallelism
- increasing number of cores on chips
- multiple tasks can be performed at the same time on different cores (improves speed; doesn't necessarily improve latency but your throughput will improve)
- Difficulties with parallelism
  - When do tasks start/stop?
  - what if one task needs data from another task?
  - Do tasks conflict in memory?

### Concurrent Programming
- Concurrency is the management of multiple tasks at the same time. (They might not be actually executing at the same time but they are *alive* at the same time)
- Key requirement for large systems
- Enables parallelism
  - Management of task execution
  - Communication between tasks
  - Synchronization between tasks

### Concurrency in Go
- Go has a lot of concurrency primitives built-in to the language and implemented efficiently
- Go routines represents a concurrent tasks, basically a thread
- Channels are used for concurrent for communication between concurrent tasks. 
- Select is used to enable synchronization.
> Having concurrency built into the language and having an efficient implementation is advantageous if you're doing concurrent programming especially with all the cores that exists in processes these days.


