# The Interview

A typical co-op interview is split into three parts.
1. recruiter screening
2. technical interview
3. behavioural interview

## Recruiter Screening

This should be straightforward "get to know you" meeting with the recruiter. This is done on the company's part to identify any early red flags and to gauge the general fit. I once applied to an engineering position only to find that it was an IT position during this stage of the interview. We both mutually agreed not to proceed with the interview and this saved a lot of people's time.

Some questions you can expect:
* Tell me about yourself
* Why did you apply here?
* What are your long-term and short-terms goals for co-op?

## Technical Interview

### Types of Questions

While most companies still adhere to algorithm questions for their technical interviews, personally I've seen a shift to more organic questions at this stage. As such, I'll provide a few examples of these types questions.

#### Algorithm

These types of questions are the ones you see on Hackerrank or Leetcode. They typically involve data structions, algorithm, and/or string manipulation. Since you can find plenty of examples online, I won't dwell on this topic for too long. 

Cracking the Coding interview does a great job of walking through a problem step-by-step. I suggest you read the section on how to answer a question. For the purpose of this post, I will summarize my approach when answering a question.

**1. Understand the question**

Unlike leetcode or hackerrank, the point of these questions is to assess your communication skill. Take time to go through the question, and clarify any assumptions. You may also request to make an assumption or narrow the range of inputs to get started, and revisit those assumptions once you have a working solution.

**2. Identify the type of question**

Is the question asking you to go through a string? Does it require a specific data structure? Can it be solved using hashmap? These types of questions usually have a pattern with similar solutions. With practice, you will begin noticing these patterns.

**3. Choose a data structure**

Most questions can be solved with just a proper selection of a data structure (e.g. stack, hash map, array). If the solution requires random access - use a hash map. If it requires remembering the order of things, use a stack or an array. Inevitably, some questions don't fall into these simple data structures, such as reversing a binary tree or traversing a linked list. 

Communicate your choice to your interviewer. Here is an opportunity to discuss that choice, and perhaps your interviewer will point you towards a more refined solution.

**4. Provide sample inputs**

Once you've decided on your data structure and before you write a line of code, you will need to provide some sample inputs. My general rule of thumb is to use one happy path input, but also generate some edge cases to test your solution. This shows that you understand how your code may fail and that you have a plan to address those scenarios.

**5. Walk through your solution**

This is where most people begin pseudocode. Pseudocode is code that is not syntactically correct, but loosely defines the behaviour for a line of code. You may even choose to do this step in plain English. Be sure to voice out your thoughts. You may find yourself stuck - and generally that's an indication that you've chosen the wrong data structure or that you've missed a step somewhere. At this point, your interviewer may step in to provide pointers, but that does not mean you've failed the interview. Interview questions are purposefully difficult to challenge candidates and interviewers know that.

**6. Validate your solution**

Revisit your sample inputs and feed your solution these inputs one-by-one. Most likely you'll have to add a few tweaks to create a working solution. If you're here, you are closer to the finish line than you think!

**7. Refine your solution**

If your code is still in pseudocode, you may be asked to rewrite it with syntactically correct code (hopefully you'll have an IDE to do this). Your interviewer may also ask extension questions. 

By this point, you're done! Congratulations!

Co-op example questions:
- Given a string, find the character that appears the most
- Given an array of numbers, write a function that accepts an index and returns the largest number up to that index
- Reverse an array. (optional) Do it in-place.

#### Debugging

These types of questions test your ability to read and to improve code. You will likely be presented with a snippet of code, and tasked to find and to fix the issue. It is possible that you may not be given an IDE for this section, so be prepared to fix the code using a white board.

For these types of questions, I like to approach it like this:
1. Understand the expected output given the input
2. Procure some sample inputs and test the output. There maybe a pattern you can derive from the outputs that can narrow the potential source.
3. Understand what each line is supposed to do. If it is a large piece of code, write comments for complex parts.
4. Walk through the entire code with a sample input. 

By now, you should have a good sense of where it went wrong and that's already half the journey. The fix will require a mixture of experience and knowledge, which is something you'll gain as you continue to practice and to code.

Example 1: Recursion
```javascript
/**
 * This function should return the n-th Fibonacci number when given n, where n >= 0
 * @param {string} n
 * @returns {number}
 */
function fibonacci(n) {
    if (n < 2) {
        return n
    }
    return findFib(n-1) + findFib(n)
}
```

Example 2: Stack
```javascript
/**
 * This function checks whether or not a string is a palindrome
 * @param {string} word
 * @returns {boolean}
 */
function isPalindrome(word) {
    for (let i = 0; i <= word.length; i++) {
        if (word.charAt(i) !== word.charAt(word.length)) {
            return false
        }
    }
    return true
}
```

#### System Design

These questions are designed to test your understanding of system architecture. These are complex questions and usually more important as you gain seniority. For my interns, my expectation is that they understand the difference between backend and frontend, how data is passed between these domains, some modern web frameworks and their differences, and general ideas on security and performance. 

An interviewer may ask you to describe a project and explain your technology choices to assess your understanding of system architecture. Be prepared to answer the following:
- Why did you choose Technology A over Technology B?
- How did you design your APIs and why did you choose this design?
- What technologies did you choose for state management?
- Did you encounter any performance issues with your appplication? How would you address them?

## Behavioural Interview

This is usually the last step of your interview. Here, you will likely meet your hiring manager and possibly one other team member. This is your chance to get to know the team and vice versa. Remember, the people across the panels were likely in your position in the past so likely they are empathetic to your situation. You can see this as an extension to the recruiter screening and this is a chance to go in-depth into your experience.

Some questions you can expect:
* Describe an instance of where you disagreed with your team
* Give me an example of a project you saw end-to-end and what were some challenging parts?
* Give me a scenario where you made a mistake. What happened and how did you deal with it?