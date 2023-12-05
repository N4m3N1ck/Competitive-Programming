# Handcrafted Gift
Url to the problem statement: https://ioi.te.lv/locations/ioi20/contest/day0/gift.pdf
## Step 1: Understand the problem statement
The problem asks us to return if it is possible to make a necklace out of blue and red beads with these requirements. The requirements are a set of ranges, and each range can have one or two unique colors.
## Step 2: Analyze some examples and notice patterns.
Take this sample necklase and the requirements: <br></br>
<img width="304" alt="image" src="https://github.com/N4m3N1ck/Competitive-Programming.md/assets/138298706/af62b307-5cc7-4d14-89dd-cd0f7a933f68"> <br></br>
- Range [0,2] can have only one unique color
- Range [2,3] can have only two unique colors
- Range [3,4] can have only one unique color
Is it possible to make such necklace? Yes. It can be either RRRBB or BBBRR.
<br></br>
Let's take another example:
- Range [0,5] - one color
- Range [1,3] - two colors <br></br>
Is this possible? No. Why? Because we can't satisfy both conditions. Why? Because two is a subrange of one. If two has two colors, then one has two colors which is not satisfying the condition. \
Why is it possible in first case but not in the other? \
In the first case, the range [2,3] is not a full subrange of [0,5] or [1,3], so it is possible to split the colors to satisfy both ranges it is a part of. 
## Step 3: Simplify the problem into subproblems
Observation 1: \
If a range of two unique colors is a subrange of one unique color, return false. (Otherwise, return true??????)\
Will every other case be true? Let's see.
Let's take this example:
<img width="413" alt="image" src="https://github.com/N4m3N1ck/Competitive-Programming/assets/138298706/d1c6291d-9d51-4814-bcfc-4ab1e0b3fc91"><br></br>
According to our established rules this is possible, right? No, it isn't. Why? \
Let's take a look at the ranges [0,3] and [3,5]. They both can have only one color. And they also intersect. What does this mean? It means that these ranges have to have the same color, which means we can count them as one range.
<img width="413" alt="image" src="https://github.com/N4m3N1ck/Competitive-Programming/assets/138298706/e25b5fb2-9242-4513-8923-2db76b05d94d"><br></br>
Does this look familiar? Yes, this is the case in which 2 is subrange of 1, and we return false. \
This is pretty much how you solve this problem. First, join all the intersecting ranges of one, and then check if there is a range of 2 unique colors which is a subrange of 1.


