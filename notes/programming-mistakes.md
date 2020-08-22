# How to program and debug more effectively as a data scientist

## Lessons from my first data science software project

Recently, I delivered my first software package, designed to automate some time-intensive calculations that are critical to my team's data workflow. The process included more debug cycles than I care to admit, partly because of growing code complexity and evolving requirements, and partly because I could have planned and executed more effectively. 

After some reflection, here are some key lessons from that experience, which can help you write software more effectively as a data scientist.

### 1. Map out your software design 

When I started my project, I dove into coding with limited upfront planning, thinking that the exact details of my software design would become clearer as I coded.  As my code became more complex, I started losing track of how all my functions fit together. 

And when requirements changed -- meaning I had to make modifications to my program's design, I wasn't completely sure how all my code fit together. Without a blueprint or diagram to refer to, I had to re-invest time sifting through code to recall how data was being passed between functions, in what format, etc.  and to refresh on the logic I used to manipulate the data.

Avoiding this pitfall takes relatively little effort. Have a simple, but clear picture of what your software does at a high-level, whether you draw out a diagram or take notes on your software's design and functions. Keeping a sketch with pen-and-paper and boxes and arrows would suffice. I personally wrote bullets on a working document that I could constantly modify. 

There are several advantages of keeping a design map. For one, documenting your software design will give you a clearer idea of how all your code pieces fit together. Verbalizing the logic of your data manipulations can help you sense check that your logic will give you your intended result. And of course, having a clear reference becomes extremely handy when you need to make bigger changes to the design of yoru code. 


### 2. Invest in file organization

Between multiple scripts and Excel files, I grossly underestimated the number of files that I would be navigating throughout my project. When my ad-hoc file naming system eventually failed, I found myself re-writing several functions because I couldn't find the original files in which I'd written them. 

Investing in your organization will inevitably reduce stress down the line, and improve long-term efficiency. Before starting a project, it's helpful to invest some upfront effort to define a clear, maintainable file organization and naming system. 

Some basics guidelines would be to have:

-  a separate folder for each project you're working on
-  a folder for each of your respective file categories (i.e. scripts, data, outputs, QA, etc.)
-  a consistent naming convention for code
-  a consistent naming convention for your data files 

Beyond that, I found it helpful to use version tags and date tags on code and data files (`v2-file-2020-08-03`), to make it easier to navigate by chronlogy.

### 3. Validate each code unit

Debugging was the most painful part of my programming project by far. This pain often stemmed narrowing down the location of bugs. One lesson I learned was to validate regularly at each transformation step, to ensure that any data processing result had values and dimensions I expected.

This allowed me to catch unexpected behavior early on, and allowed me to be confident about data at each step.

A couple basic checks that I regularly used: 

- Checking number of rows before and after joining two data frames
- Checking that sums of variables match up before and after processing
- Regularly checking form missing values 

To increase efficiency and repeat keystrokes, I would think about ways to automate validation, either through by creating simple validation functions or Excel templates. For me, time invested in automating validation easily paid itself off tenfold.

### 4. Debug methodically 

When errors arise, debugging by following your instincts can sometimes pay off. But without a plan, this approach can be arbitrary and frustrating. In the long-term, following a methodical debugging procedure is a more effective strategy. 

Building a system in which you narrow down sources of error and document attempted solutions can help you more effectively circle in on a solution. Moreover, this keeps stress at bay, allowing you to focus on debugging with an organized and calm mind.

At a high-level, I think a system should involve understanding the error message, developing context around the bug, and testing and documenting solutions in an organized fashion. In this system, you get more control over your debugging process, a reference document for future debugging cycles, and significant reduction in stress in exchange for a small additional investment in time and effort. The procedure that I've been using is:  

1. If there is an error message, read it carefully and look it up; if not, describe the unexpected behavior in writing
2. Narrow down the location of the offending code by inserting manual tests
3. Once you've identified where the error occurs, check the structure, format, and values of the data entering your offending code -- usually this will lead to a solution
4. Fix, re-run, evaluate, document
5. If the error persists, research the error further and test again
6. If the error persists, ask for debugging help 

While your system might be different, I think the core principles will be the same: understand your error, locate the bug, investigate obvious sources of error, and test and document.

### 5. Record your solutions 

- Had to repeat
- I have had to debug same error twice
- Avoid debugging the same error twice 
- If you have ever debugge Have you ever debugged the same problem
- Solutions reference = greater efficiency
- Suggestion: track all errors in a Google sheet

This was important enough that I want to reiterate it as its own point. Keeping a growing list of solutions lets you be more efficient moving forward.

The same bugs will often pop up in your code, and to avoid researching the same issues over and over again, I recommend tracking the solutions you've used.

By keeping the details of previously used solutions, you keep a growing log of issues that keeps you from repeating efforts with stuff. 

My suggestion is to keep track of each error you face in a Google sheet, and keep it simple. Include the date of the problem, your error code and where it occurred, and the solution that you ended up using. 


