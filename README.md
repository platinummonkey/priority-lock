# Overview

Go Implmentation of a priority locks.

# Implementations

## Triple Mutex

Uses 3 mutexes to lock. Very basic and simple to reason about.

# TODO

## Implementations

### Priority queue lock

This would allow for a Priority FIFO-like queue of workers to obtain the lock to prevent any one worker from hogging requests, and give more priority to high priority workers.

