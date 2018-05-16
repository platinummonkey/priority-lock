# Overview

Go Implmentation of a priority locks.

# Implementations

## Priority Preference Lock

Uses 3 mutexes along with a high priority counter to lock. Very basic and simple to reason about.
This will generally force low priority lockers to wait until the high
priority queue is drained before they are able to access the underlying
lock. High priority locks will have preference.


# Example Usage

```

lock := NewPriorityPreferenceLock()

// Assuming low priority tasks take some reasonable amount of time
for _, t := myLowPriorityTasks {
  go func(t, lock)
}

// assuming high priority tasks are important to interrupt low priority
// inter-operations.
for _, t := myHighPriorityTasks {
  go func(t, lock)
}
```
