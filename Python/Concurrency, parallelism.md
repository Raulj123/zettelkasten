==I/O :== "eye-oh," describes any operation, program or device that transfers data to or from a computer.
==synchronous:==  "sequential", because the computer / program follows all the steps in sequence before switching to a different task, even if those steps involve waiting.
# Asynchronous Code
asynchronous code lets the program multitask: it does other work while waiting for something to finish. Waiting for something else refers to I/O operations like("I/O bound" operations):
* the data from the client to be sent through the network
- the data sent by your program to be received by the client through the network
- the contents of a file in the disk to be read by the system and given to your program
- the contents your program gave to the system to be written to disk
- a remote API operation
- a database operation to finish
- a database query to return the results
- etc.

This idea of **asynchronous** code described above is also sometimes called **"concurrency"**. It is different from **"parallelism"**.

# Concurrency vs Parallelism
- **Concurrency**: Interruptability
- **Parallelism**: Independentability

## Concurrency 
You carry a laptop with you, and while waiting in the line, you start working on your presentation. This way, once you get back at home, you just need to work 1 extra hour instead of 5.

In this case, both tasks are done by you, just in pieces. You interrupted the passport task while waiting in the line and worked on presentation. When your number was called, you interrupted presentation task and switched to passport task. The saving in time was essentially possible due to interruptability of both the tasks.

## Parallelism
u’re obviously a higher-up, and you have got an assistant. So, before you leave to start the passport task, you call him and tell him to prepare first draft of the presentation. You spend your entire day and finish passport task, come back and see your mails, and you find the presentation draft. He has done a pretty solid job and with some edits in 2 more hours, you finalize it.

Now since, your assistant is just as smart as you, he was able to work on it _independently_, without needing to constantly ask you for clarifications. Thus, due to the independentability of the tasks, they were performed at the same time by _two different executioners_.

https://stackoverflow.com/questions/1050222/what-is-the-difference-between-concurrency-and-parallelism

With **FastAPI** you can take advantage of concurrency that is very common for web development (the same main attraction of NodeJS).

But you can also exploit the benefits of parallelism and multiprocessing (having multiple processes running in parallel) for **CPU bound** workloads like those in Machine Learning systems