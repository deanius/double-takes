---title: "Double Down on Testing With RxJS Load Tests"date: "2017-03-20"author:  name: "Dean Radcliffe"  url: "http://twitter.com/deaniusaur"tldr:  title: "RxJS can make for great load tests"  body: """Learn some strategies for testing with this example of RxJS code that tests a WebSocket-based site.        """---At Test Double, we love to test. Know about the Testing Pyramid, and use it. And, we'll roll our own testing code if we need to.

Now- much of the testing pyramid focuses on correctness. Has Pass / Fail outcomes. Even aims to affect naming in pieces of code. Yet, sites with tons of these tests still fail in production - why? Every test they have is still screaming 'Green', while the email boxes fill up with complaints. Enter Load Testing, the orphan step-child of the testing suite. 

Load testing deals not in black and white, but shades of gray, and pesky floating point numbers. It can be tricky to write - it's some of the most concurrent, distributed, error-tolerant code you'll ever need to write! And that's why, when my toolchest of common testing tools failed to produce a fit to my latest testing problem, I relished the chance to whip one up myself. Fortunately it took less than half a day until these tests revealed their dividends.

Here's how this bad-boy looked, configured to 4 agents, 12 tasks each.

![](../img/rxjs-load-test-run.gif)

* TODO Describe some existing non-custom solutions like `ab`]

* TODO Describe what to look for in the results, and why 'average' is a useless statistic]

* TODO Step through the code [here](https://gist.github.com/deanius/6284d7b8d634b6f0bb8ae28a063a21a1#file-loadtest-js ), hand-waving over the fact that this is not easy to write!]

* TODO Describe the parameters available for tweaking, and hand-wave over the fact they're hard-coded in 
