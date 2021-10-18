# Reading Notes
A collection of notes and take-aways throughout my Code 401 journey.
## Code 401 - Advanced Software Development

- [Articles](#articles)
- [Videos](#videos)

## Articles

- [Solving Problems](#solving-problems)
- [Act like you make $1000/hr](#act-like-you-make)
- [How to think like a programmer](#how-to-think-like)
- [The 5 Whys](#the-5-whys)

### Solving Problems
[source](https://simpleprogrammer.com/solving-problems-breaking-it-down/) -John Sonmez

    When solving programming problems, it is important to understand the problem before you ever try to write code for a solution. The author of this article provides the following steps to follow for most problems:

    1. Read the problem completely twice.
    2. Solve the problem manually with 3 sets of sample data.
    3. Optimize the manual steps.
    4. Write the manual steps as comments or psuedo-code.
    5. Replace the comments or psuedo-code with real code.
    6. Optimize the real code.

    The overall emphasis here is to put as much thought and attention into understanding the problem, breaking it down into manageable pieces, understanding the steps that need to happen to solve each piece, optimizing those steps for simplicity and ease of understanding.

### Act like you make $1000/hr
[source](https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d) -Anthony Moore

    This article explains the benefits of spending your time wisely. The overriding suggestion is to consider your time to be worth $1000/hr, and judge each moment by whether or not is living up to that figure.

    An interesting point that the author makes is that you should say "no" to things that are either not worth your time or don't work towards achieving your goals. By overextending yourself, you can take away from the thigs that you really need to focus on.

    Another point of intereset is that you should stay focused, rather than allowing yourself to get lost in something. The suggestion is that you should always strive to pay attention to what you are doing and why, so that you don't get distracted or bogged down by meaningless details. The author states "If you don't manage your time, it will manage you."

### How to think like a programmer
[source](https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2/) -Richard Reis

    Thinking like a programmer means being able to more effectively solve problems. This means avoiding common pitfalls like getting stuck in a loop of trying solutions until something fits, and establishing a framework from which you can navigate any problem, no matter the complexity.

    The suggested steps are:

    1. Understand

        Use whatever approach you need to in order ensure that you understand the problem. Write it out, diagram, talk it over with someone or something, do what you need.

    2. Plan

        Once you understand the problem, you need to plan your solution. Takew the time to identify how you can get from point a to point b. An example provided by the author is "Given input X, what are the steps necessary to return output Y?"

    3. Divide

        This step is both straight-forward and essential. Break the problem into smaller, more easily solved problems, then connect the solutions together.

    4. Stuck?

        If you try and try, but can't find the solution to a problem, the author three very useful suggestions:
        - Debug: Take a look at each step of your solution to ensure that it works as intended.
        - Reassess: Try approaching the problem differently.
        - Research: Chances are, someone has probably already solved a similar problem.

### The 5 Whys
[source](https://www.mindtools.com/pages/article/newTMC_5W.htm)

    This article explains a method of addressing problems that require more than just a "quick fix". The overall idea is to gather a group of subject-matter experts to "go and see" the problem in action, evaluate what the problem appears to be, then ask "why?" until they get to the root of the problem. Then, an effective counter-measure can be identified and employed to prevent the problem from happening again in the future.

    Here's an example they provided of what that process might look like:

![5-whys-diagram](/img/5-whys-single-lane.png)

    A couple of useful tips that they provided are:
    - The "5" is just a suggestion, more or less "why's" may be needed.
    - While the immediate answer to a "why" may fall directly on someone's actions or lack thereof, the 5 Whys process enables you to keep asking why until you can find an organizational problem.

## Videos

- [what the heck is the event loop anyway](#what-the-heck-is-the)
- [The Super Mario Effect](#the-super-mario-effect)

### what the heck is the event loop anyway
[source](https://www.youtube.com/watch?v=8aGhZQkoFbQ)

    This video explained how JavaScript interacts with the browser to effectively let more than one thing happen at a time. This is an important concept, because JavaScript itself can only run one thing at a time, which would potentially drastically interfere with a user's experience.

    Essentially, as asynchronous callbacks are executed, they get passed to a web api, which the browser keeps track of and handles independently of the JavaScript stack. When the conditions are met for the callback, it is passed to the callback queue, where it waits its turn to be sent back to the JavaScript stack. The event loop waits until the stack is empty, then sends the first item in the callback queue to the stack.

### The Super Mario Effect
[source](https://www.youtube.com/watch?v=9vJRopau0g0)

    In this video, Mark Rober explains how changing your changing your reaction to failure can ultimately lead to success. He used an example set of data that he collected to show that people who are not concerned with the negative ramifications of failure can bounce right back and try again until they get it right. He then gave many examples from his own life and experiences, reinforcing the idea that you should embrace failure and learn from it, rather than be ashamed or give up.