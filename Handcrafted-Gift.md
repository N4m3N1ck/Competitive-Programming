# Handcrafted Gift
Url to the problem statement: https://ioi.te.lv/locations/ioi20/contest/day0/gift.pdf
## Step 1: Understand the problem statement
The problem asks us to return if it is possible to make a necklace out of blue and red beads with these requirements. The requirements are a set of ranges, and each range can have one or two unique colors.<br>
## Step 2: Analyze some examples and notice patterns.
Take this sample necklase and the requirements:<br>
<br>
<img width="304" alt="image" src="https://github.com/N4m3N1ck/Competitive-Programming.md/assets/138298706/af62b307-5cc7-4d14-89dd-cd0f7a933f68"> <br>
- Range [0,2] can have only one unique color
- Range [2,3] can have only two unique colors
- Range [3,4] can have only one unique color
Is it possible to make such necklace? Yes. It can be either RRRBB or BBBRR. <br>
Lets take another example: <br>
<br>
<img width="301" alt="image" src="https://github.com/N4m3N1ck/Competitive-Programming.md/assets/138298706/098f50a5-32fb-4f4f-82dc-87cb427833e3"> <br>
<br>
It is not possible to make such a necklace, because range that requires two colors is a subrange of a range which requires one color, which is an impossible condition to satisfy
## Step 3: Simplify the problem into subproblems
