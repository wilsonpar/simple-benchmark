# simple-benchmark



Simple Benchmarking Tools Documentation
This documentation provides an overview of the Simple Benchmarking tools implemented in Unreal Engine. These tools are designed to measure the execution time of functions or delegates, offering both synchronous and asynchronous options.

1. Calculate Delegate Execution Time
Functionality: Synchronously calculates the execution time of a given delegate.
Usage: Useful for performance measurement in a blocking manner. It returns the execution time directly.
Parameters:
DelegateToExecute: The delegate to be executed and measured.
TimeUnit: The unit of time measurement (Nanoseconds, Microseconds, Milliseconds, Seconds, Minutes, Hours).
Return Value: Execution time in the specified time unit.
Visual Representation:
![2](https://github.com/wilsonpar/simple-benchmark/assets/152873301/34beaa40-6438-421d-bd02-3cb2f3f7e86c)


2. Calculate Execution Time with Callbacks
Functionality: Calculates the execution time of a delegate, allowing for additional functions to be executed before and after the main delegate.
Usage: Ideal for scenarios where setup or cleanup operations are needed alongside the performance measurement.
Parameters:
PreExecutionCallback: A delegate to execute before the main delegate.
Main: The primary delegate whose execution time is measured.
PostExecutionCallback: A delegate to execute after the main delegate.
TimeUnit: The unit of time measurement.
Return Value: Execution time of the main delegate in the specified time unit.
Visual Representation:
![3](https://github.com/wilsonpar/simple-benchmark/assets/152873301/0110d104-9956-430c-bec0-e34ba57e83d9)

3. Calculate Execution Time Async
Functionality: Asynchronously calculates the execution time of a delegate.
Usage: Suitable for non-blocking performance measurement, where the main game loop should not be interrupted.
Parameters:
DelegateToExecute: The delegate to be executed and measured asynchronously.
CompletionCallback: A callback delegate that is executed with the execution time once the measurement is complete.
TimeUnit: The unit of time measurement.
Return Value: None. The execution time is passed to the CompletionCallback.
Visual Representation:
![4](https://github.com/wilsonpar/simple-benchmark/assets/152873301/e15ad030-484f-4a41-95e4-13e7dadb769f)


4. Calculate Execution Time Async With Callbacks
Functionality: Asynchronously calculates the execution time of a delegate, including optional pre-execution and post-execution callbacks.
Usage: Best for when additional operations need to be performed before and after the main asynchronous task, without blocking the main thread.
Parameters:
PreExecutionCallback: A delegate to execute before the main delegate.
MainDelegate: The primary delegate to be executed asynchronously.
PostExecutionCallback: A delegate to execute after the main delegate.
CompletionCallback: A callback delegate for when the measurement is complete.
TimeUnit: The unit of time measurement.
Return Value: None. The execution time is passed to the CompletionCallback.
Visual Representation:
![5](https://github.com/wilsonpar/simple-benchmark/assets/152873301/de48993d-cb34-410c-9188-5d88ebffbdce)
