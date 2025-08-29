# Design and Analysis of Algorithms

# Week 6

# Programming Assignment

```bash
def max_events(events):
    # Step 1: Compute end times and store them along with start times
    events = [(start, start + duration - 1) for start, duration in events]
    
    # Step 2: Sort events by their end times (second element of tuple)
    events.sort(key=lambda x: x[1])
    
    # Step 3: Greedy selection of events
    count = 0
    last_end_time = -1
    
    for start, end in events:
        if start >= last_end_time:
            # Select this event
            count += 1
            last_end_time = end  # Update the end time of the last selected event
    
    return count

# Input reading function
def main():
    N = int(input())  # Number of events
    events = []
    
    for _ in range(N):
        start, duration = map(int, input().split())
        events.append((start, duration))
    
    # Get the maximum number of events that can be scheduled
    result = max_events(events)
    
    # Output the result
    print(result)

# Run the main function
if __name__ == "__main__":
    main()

```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
