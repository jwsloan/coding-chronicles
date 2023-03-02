# Down the Rabbit Trail

I thought that my second post would dive right into using generators in Python. However, in an attempt to be understood, I tend to provide a lot of context around some topic before discussing the actual topic. The fact that the [Getting Started](../2023_02_27_getting_started/) post exists at all is evidence of that. 

The particular generator use case that I would like to illustrate does not exist in isolation. When I used the pattern, it was in some real-world production code. That particular code runs in an [AWS Lambda](https://aws.amazon.com/lambda/), and is is writing data to a [DynamoDB](https://aws.amazon.com/dynamodb/) database using the [Single Table Design](https://www.alexdebrie.com/posts/dynamodb-single-table/) pattern. 

The Lambda in question makes use of the [Functional Core, Imperative Shell](https://www.destroyallsoftware.com/screencasts/catalog/functional-core-imperative-shell) design pattern, which allows us to write highly testable, readable, changeable code. 

All of the concepts I've linked to above are interesting, and deserve posts of their own. The internet is full of articles and tutorials dedicated to these concepts, but I want to at least touch on some of them so that my use of a generator in this case might be better understood. 

To that end, I'm going to take you along a bit of a rabbit trail. We will find our generator function along the path. I don't yet know if we'll stop there, but we should get there.

## Notes About the Path

What I am going to describe in this series of posts is not THE way to solve this problem. The problem itself is contrived and considerably simpler than the actual problem solved by the production code inspiring this series of posts. There are many reasonable ways one might solve the problem. I'm not saying that these are the best patterns to follow in all cases, or even in this case, but I have found these patterns to be very helpful in my day-to-day, and so would like to share about them here.


# User Service

What we're going to work through is a very simple User Service. It will get more complex as we go along, but it at least starts out  fairly simply. 


* [Part One](./part1/README.md)
