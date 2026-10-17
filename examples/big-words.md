# Big words

**Question:** Why is my page slow?

## Before

> To facilitate a comprehensive understanding of the performance bottleneck, it's crucial to delve into the nuanced interplay between your rendering pipeline and data-fetching layer. By leveraging robust profiling tools, you can ensure a seamless diagnosis.

## After

> You fetch the user list one row at a time. That is 200 requests. Fetch them in one call.

The second one is shorter and names the actual problem.
